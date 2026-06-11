# Printable PDF Formatting

Use this reference when a user asks for a directly printable Chinese government document PDF or complains that title, font, line spacing, margins, or page width do not meet official formatting expectations.

## Baseline Formatting

Use GB/T 9704-2012-style assumptions unless a local template is provided:

- A4 paper.
- Left binding.
- Margins commonly used by the standard template: top about 37 mm, bottom about 35 mm, left about 28 mm, right about 26 mm.
- Body grid: generally 22 lines per page and 28 Chinese characters per line.
- Title: generally 2号小标宋体.
- Body: generally 3号仿宋体.
- First-level headings: commonly 黑体.
- Second-level headings: commonly 楷体.
- Page numbers: centered or template-positioned Arabic numerals, in the official style such as `— 1 —`.
- Document number year must use six-angle brackets `〔〕`.

## Font Rules Learned From Practice

- Do not assume macOS has 仿宋 or 楷体 installed. Check fonts before generating.
- Microsoft Office for Mac may include `Fangsong.ttf` and `Kaiti.ttf` under app resources. If legally available on the user's machine, install/copy to the user font directory before generation.
- On macOS, `Songti.ttc` subfont index 0 may be a black/bold Songti face; using it for body text can make the whole document look incorrectly bold.
- Some system Chinese fonts render `〔〕` like square brackets. Test `某政办发〔2026〕12号` visually before final delivery.
- If using ReportLab, register exact font files and use explicit font names. Do not rely on fallback fonts.

## PDF Generation Checklist

Before delivery:

1. Confirm page geometry: A4, margins, body width.
2. Confirm title font is 小标宋 or the closest installed official title font.
3. Confirm body font is 仿宋, not 宋体/黑体 fallback.
4. Confirm line grid: 22 lines per page and about 28 Chinese characters per line.
5. Confirm document number uses `〔〕`.
6. Confirm first page has red heading, red separator, document number, title, main recipient, body, issuing body, date, and disclosure note when appropriate.
7. Confirm attachment title and body continue in official format.
8. Confirm appendix tables do not overflow the page width.
9. Render or preview the PDF visually; text extraction alone can miss layout and font errors.

## Fixed-Grid Warning

Free-flow paragraph layout often fails official formatting requirements because it lets the renderer choose line breaks, line spacing, and glyph fallback. For strict official PDFs, prefer fixed geometry:

- Calculate body frame from margins.
- Set line pitch from 22 lines per page.
- Set character pitch from 28 Chinese characters per line.
- Wrap Chinese text manually and avoid punctuation at line start.
- Draw page numbers consistently.

If fixed-grid drawing causes awkward text extraction, explain that visual print fidelity was prioritized.
