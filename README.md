# Staggered Difference-in-Differences (DiD)

## Project Overview

This project **partially replicates** the results from **Gilraine, Macartney, and McMillan (2018)** and **extends their analysis** using a **staggered Difference-in-Differences (DiD)** framework.

The original paper introduces a method to jointly estimate the **direct and indirect effects** of major education reforms, focusing on **California’s Class Size Reduction (CSR) program** — a statewide initiative launched in the late 1990s that incentivized public schools to reduce class sizes to **20 or fewer students in grades K–3**, with a **staggered rollout** beginning in **1996–97**.

While this replication closely follows the paper’s methodology, **some results may slightly differ** because a different software environment is used compared to the original authors.

## Dataset

The dataset used is `PS2 data.csv` located in the data folder, which contains:

- `district_code`: District identifier
- `grade`: Grade level (K–3)
- `year`: School year (fall year; e.g., 1990 = 1990–91)
- `share`: Private school share
- `enr`: Total district enrollment (private + public)
- Demographic controls:
  - `pctep`, `asianpct`, `hisppct`, `afampct`, `whitepct`, `pacificpct`, `nativepct`, `malepct`

## About Difference-in-Differences (DiD)

**Difference-in-Differences (DiD)** is a popular econometric technique used to estimate causal effects by comparing changes in outcomes over time between a **treated group** and a **control group**. 

## Key Methodological Steps

- **Defining Event Time**:
  - Treatment introduced:
    - Grade 1: 1996
    - Grade 2: 1997
    - Grade 3: 1998
    - Kindergarten: 1998
  - An **event time variable** aligns treatments to a common period 0.

- **Analysis Progression**:
  - **Basic Two-Period DiD**: Simple before-and-after comparison.
  - **TWFE DiD**: Two-Way Fixed Effects model including district and year fixed effects.
  - **Stacked DiD**: Extension for staggered treatment timing across grades.

- **Parallel Trends Check**:
  - **Event-study plot** produced to test for pre-treatment trend similarity.

## Notes

- This project walks through each method step-by-step for educational purposes.
- Minor differences in results are expected compared to the original study.
- **Treatment** is defined as **class size reduction** under California’s CSR program.
- Some understanding in statistics and coding is expected to complete the project. 

## Reference

Gilraine, Michael, Macartney, Hugh, and McMillan, Robert. (2018). *Education Reform and the Structure of the American Family*.
https://www.nber.org/system/files/working_papers/w24191/w24191.pdf
