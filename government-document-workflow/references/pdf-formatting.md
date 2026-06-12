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
- Microsoft Office for Mac may also include `SimHei.ttf`. Prefer this or another standard SimHei/黑体 face for first-level headings when the system `STHeiti` punctuation glyphs look wrong.
- On macOS, `Songti.ttc` subfont index 0 may be a black/bold Songti face; using it for body text can make the whole document look incorrectly bold.
- Some system Chinese fonts render `〔〕` like square brackets. Test `某政办发〔2026〕12号` visually before final delivery.
- Some macOS Chinese black fonts render the dunhao `、` in first-level headings as a centered or horizontal-looking mark. In public official PDFs, first-level headings such as `一、总体要求` use the standard font glyph, not a hand-drawn replacement. If the dunhao looks wrong, switch the heading font to a better standard黑体/SimHei rather than manually drawing punctuation.
- If using ReportLab, register exact font files and use explicit font names. Do not rely on fallback fonts.

## Heading Punctuation Rules

For first-level headings:

- Use the text form `一、标题`, `二、标题`, `三、标题`.
- Do not write `一. 标题`, `一．标题`, `一 标题`, or split the number and title with a comma-like hand-drawn mark.
- Do not draw `、` manually as a line or shape. Public official PDFs show a real font glyph.
- Use a standard black heading font and render the whole heading naturally. On macOS, prefer Office-provided `SimHei.ttf` over `STHeiti` if `STHeiti` places `、` incorrectly.
- Compare visually against a public official PDF that contains `一、总体要求` before delivery when the user has raised punctuation or heading-format concerns.

For attachment lists:

- Use Chinese official-document numbering such as `附件：1．...` and subsequent aligned lines `2．...`, `3．...` when a local template does not specify otherwise.
- Avoid half-width `1.` in printable official PDFs.

## PDF Generation Checklist

Before delivery:

1. Confirm page geometry: A4, margins, body width.
2. Confirm title font is 小标宋 or the closest installed official title font.
3. Confirm first-level heading font is standard黑体/SimHei and that `一、总体要求` uses a proper dunhao glyph.
4. Confirm body font is 仿宋, not 宋体/黑体 fallback.
5. Confirm line grid: 22 lines per page and about 28 Chinese characters per line.
6. Confirm document number uses `〔〕`.
7. Confirm first page has red heading, red separator, document number, title, main recipient, body, issuing body, date, and disclosure note when appropriate.
8. Confirm attachment title and body continue in official format.
9. Confirm appendix tables do not overflow the page width.
10. Render or preview the PDF visually; text extraction alone can miss layout, font, and punctuation-glyph errors.

## Fixed-Grid Warning

Free-flow paragraph layout often fails official formatting requirements because it lets the renderer choose line breaks, line spacing, and glyph fallback. For strict official PDFs, prefer fixed geometry:

- Calculate body frame from margins.
- Set line pitch from 22 lines per page.
- Set character pitch from 28 Chinese characters per line.
- Wrap Chinese text manually and avoid punctuation at line start.
- Draw page numbers consistently.

If fixed-grid drawing causes awkward text extraction, explain that visual print fidelity was prioritized.
