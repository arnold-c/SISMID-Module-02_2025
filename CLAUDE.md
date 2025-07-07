# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Quarto-based educational website for SISMID Module 2: Mathematical Models of Infectious Diseases (2025). The project contains lecture materials, R exercises, and interactive tutorials focused on epidemiological modeling using R.

## Development Commands

### Building and Rendering
- **Render the entire book**: `quarto render`
- **Preview during development**: `quarto preview` (starts local server with live reload)
- **Render single file**: `quarto render filename.qmd`
- **Check Quarto project**: `quarto check`

### R Environment Management
- **Restore R packages**: `renv::restore()` (in R console)
- **Update package snapshot**: `renv::snapshot()` (in R console)
- **Check R package status**: `renv::status()` (in R console)

### Git Workflow
- Standard git workflow applies
- The project uses renv for package management, so ensure `renv.lock` is committed when adding new R packages

## Architecture

### Content Structure
- **Lectures**: `L01_intro-to-modeling.qmd` through `L08_stochastic-models.qmd` - Main lecture content
- **R Sessions**: `r-session-01.qmd`, `r-session-02.qmd`, `r-session-03.qmd` - Hands-on R exercises
- **Prerequisites**: Setup guides for R, RStudio, and basic R programming
- **Data**: Located in `data/` directory with CSV and RData files for exercises

### Quarto Configuration
- Main config in `_quarto.yml` defines book structure, themes, and rendering options
- Custom styling in `format/` directory with SCSS files for light/dark themes
- Extensions in `_extensions/` for additional functionality like line highlighting
- Caching enabled via `execute: cache: true` in `_quarto.yml`

### R Environment
- Uses renv for reproducible package management
- Key packages: tidyverse, deSolve, diagram, gt, ggtext, here, rio
- R version 4.5.1 specified in `renv.lock`

### Output Structure
- Rendered content goes to `_book/` directory
- Figures cached in `_freeze/` and `*_files/` directories
- Site assets in `_book/site_libs/`

## Key Patterns

### Content Files (.qmd)
- All use Quarto markdown format combining markdown with executable R code chunks
- Code chunks use `{r}` syntax with options like `#| eval: false` for non-executed examples
- Heavy use of callout boxes for instructions and notes using `:::{.callout-note}` syntax

### Data Loading
- Exercises designed to load data via URLs for portability
- Alternative local file loading commented out using `here::here("data", ...)` pattern
- Data files include epidemiological datasets (flu.csv, niamey.csv) and contact matrices

### Styling and Theming
- Custom SCSS files for consistent branding with SISMID color scheme
- Responsive design with configurable sidebar, body, and margin widths
- Code syntax highlighting with custom light/dark theme support

## Working with This Codebase

When modifying content:
1. Edit the appropriate `.qmd` file for lecture content or exercises
2. Test changes with `quarto preview` to see live updates
3. For new R packages, update both the code and run `renv::snapshot()`
4. Maintain the existing callout and formatting patterns for consistency

When adding new lectures or sessions:
1. Create new `.qmd` file following naming convention (L##_ or r-session-##)
2. Update `_quarto.yml` to include in book chapters structure
3. Follow existing patterns for R code chunks and callout formatting