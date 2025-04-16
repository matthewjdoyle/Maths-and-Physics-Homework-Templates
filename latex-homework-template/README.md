# LaTeX Homework Template

A LaTeX template for generating physics and mathematics homework.

## Directory Structure

- `main.tex` - The main document file that loads the style and includes the homework content
- `homework_content.tex` - Contains the actual homework problems and solutions
- `styles/hwtemplate.sty` - Style file with all formatting and custom environments

## How to Use

1. **Setup**:
   - Edit the title in `main.tex` to set your homework number
   - Fill in the student information in the `\makeheader{}` command

2. **Adding Problems**:
   - Edit `homework_content.tex` to add your homework problems
   - Use the provided environments:
     - `problem` for individual problems
     - `part` for multi-part problems
     - `solution` for solution spaces

3. **Compiling**:
   - Compile using pdfLaTeX (or similar)
   - Make sure the style file is in the correct directory
   - You can use the included `compile.sh` script

## Example Usage

### Single Problem
```latex
\begin{problem}{10}
  Find the derivative of $f(x) = 3x^4 - 2x^3 + 5x^2 - 7x + 4$.
  \begin{solution}
    % Solution goes here
  \end{solution}
\end{problem}
```

### Multi-part Problem
```latex
\begin{problem}{15}
  Problem statement here...
  
  \begin{part}{a}{Calculate something...}{5}
    \begin{solution}
      % Solution goes here
    \end{solution}
  \end{part}
  
  \begin{part}{b}{Calculate something else...}{5}
    \begin{solution}
      % Solution goes here
    \end{solution}
  \end{part}
\end{problem}
```

## Environment Parameters

- `\begin{problem}{marks}`
  - `marks` - Total marks for the problem

- `\begin{part}{letter}{description}{marks}`
  - `letter` - Part identifier (a, b, c, etc.)
  - `description` - Text description of the part
  - `marks` - Marks allocated to this part

- `\begin{solution}`
  - No parameters, creates a styled solution box

## Notes

- The template automatically handles:
  - Formatting and styling consistent with the original markdown template
  - Numbering of problems
  - Mark allocation display
  - Header and footer formatting

## Requirements

- A LaTeX distribution (TeXLive, MiKTeX, etc.)
- The following packages:
  - geometry
  - setspace
  - amsmath, amssymb, amsthm
  - xcolor
  - fancyhdr
  - titlesec
  - enumitem
  - mdframed
  - lineno 