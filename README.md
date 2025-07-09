# SISMID Module 1 Materials (2025)

**Mathematical Models of Infectious Diseases**

This repository contains the educational materials for the [2025 Summer Institute in Statistics and Modeling in Infectious Diseases (SISMID) Module 1: Mathematical Models of Infectious Diseases](https://sph.emory.edu/SISMID/modules/math-models/index.html). The materials are presented as an interactive Quarto book website with lecture notes, hands-on R exercises, and comprehensive tutorials for epidemiological modeling.

## About This Project

This educational resource provides a comprehensive introduction to mathematical modeling of infectious diseases, covering fundamental concepts from basic SIR dynamics to advanced topics like stochastic models and parameter estimation.
The materials are designed for a 3-day intensive workshop format but can also be used for self-paced learning.

### Content Overview

The materials are organized into three main sections:

**Pre-Requisites**: Setup guides and foundational knowledge
- R and RStudio installation
- Essential R programming concepts
- Project organization best practices

**Day 1**: Introduction and Basic Models
- Introduction to modeling concepts
- Basic SIR dynamics
- Herd immunity and vaccination strategies

**Day 2**: Advanced Modeling Concepts
- Heterogeneity in models
- Age-structured models
- Parameter estimation techniques

**Day 3**: Stochastic Models and Applications
- Stochastic modeling approaches
- Advanced R exercises and applications

### Who Is This For & Pre-Requisite Knowledge?

This material is designed for:
- Graduate students and researchers in epidemiology, public health, or related fields
- Practitioners working in infectious disease modeling
- Anyone interested in learning mathematical approaches to understanding disease transmission

**Prerequisites:**
- Basic understanding of calculus and differential equations
- Familiarity with R programming (see the ["Just Enough R" section](https://sismid2025.callumarnold.com/just-enough-r) if you're new to R)
- Working installation of R and RStudio
- Approximately 30-60 minutes for setup and prerequisite review

## Getting Started

### Download and Build the Website

1. **Clone the repository:**
   ```bash
   git clone https://github.com/arnold-c/SISMID-Module-02_2025.git
   cd SISMID-Module-01_2025
   ```

2. **Install R dependencies:**
   This project uses `renv` for reproducible package management. In R:
   ```r
   # Install renv if you don't have it
   install.packages("renv")

   # Restore the project library
   renv::restore()
   ```

3. **Install Quarto:**
   Download and install Quarto from [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)

4. **Build the website:**
   ```bash
   # Render the entire book
   quarto render

   # Or preview with live reload during development
   quarto preview
   ```

5. **View the website:**
   Open `_book/index.html` in your browser, or use the local server from `quarto preview`

### Development Workflow

- **Live preview**: `quarto preview` - starts a local server with automatic reload
- **Render single file**: `quarto render filename.qmd`
- **Check project**: `quarto check`
- **Update R packages**: `renv::snapshot()` after adding new packages

## Built With

- [Quarto](https://quarto.org) - Scientific and technical publishing system
- [R](https://www.r-project.org/) - Statistical computing and graphics
- [renv](https://rstudio.github.io/renv/) - Reproducible R package management
- Key R packages: `{tidyverse}`, `{deSolve`}, `{ggplot2`}, `{gt`}, and more (see `renv.lock`)

## Contact

You can contact me via my email: "contact *at* callumarnold *dot* com".

## Contributing

We welcome contributions to improve these educational materials! Here are several ways you can help:

### Reporting Issues
- **Found a bug or error?** Open an [Issue](https://github.com/arnold-c/SISMID-Module-01_2025/issues) describing the problem
- **Have a suggestion?** Start a [Discussion](https://github.com/arnold-c/SISMID-Module-01_2025/discussions) to share your ideas
- **Unclear instructions?** Let us know what could be explained better (open a [Discussion](https://github.com/arnold-c/SISMID-Module-01_2025/discussions))

### Contributing Code or Content
1. **Fork the repository** and create a feature branch
2. **Make your changes** following the existing style and structure
    - The R code uses the [Air](https://posit-dev.github.io/air/) formatter for the R code chunks. Please follow the instructions on their website for the best way to employ the formatter in your development environment.
3. **Test your changes** by rendering the affected pages with `quarto render`
4. **Submit a Pull Request** with a clear description of your changes

### Content Guidelines
- Follow the existing Quarto markdown format and callout patterns
- Test all R code chunks to ensure they execute correctly
- Maintain consistency with the educational tone and level
- Include appropriate citations for new references

### Development Setup for Contributors
- Ensure you can successfully run `quarto preview` and `renv::restore()`
- Check that your changes don't break existing functionality
- Follow the project's code style and organization patterns

**Interested in contributing substantial content?** Please reach out to me first by opening a discussion on this GitHub page (and @ me) so we can coordinate efforts and ensure your contributions align with the overall educational goals.

## Acknowledgements

## License

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.
