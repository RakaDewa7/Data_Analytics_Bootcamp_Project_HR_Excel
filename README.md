# Unlocking Best Talents: HR Workforce Analysis

## Overview
An Excel-based analysis of 3,000 employee records to evaluate whether a company has successfully recruited and strategically placed high-performing talent  and whether it is able to retain them. The analysis centers on a single hypothesis: if high performers are concentrated in one department due to gender stereotypes, the company is unintentionally locking away its own innovation potential.

## Problem Statement
In a competitive market, operational excellence is no longer optional. Companies that lead are those that turn human capital into innovation drivers. This project investigates three questions across the employee lifecycle:

1. **Entry** : Has the company recruited quality talent proportionally across genders?
2. **Growth** : Are there gender-based barriers preventing high performers from reaching strategic roles (IT, Executive)?
3. **Exit** : Is the company able to retain its best talent, or is it losing them?

## Dataset
- **Source:** Kaggle (HR employee records, US-based company)
- **Size:** 3,000 rows × 26 columns
- **Key attributes:** EmpID, GenderDesc, DepartmentType, TerminationType, PerformanceScore (1–4 scale)

## Data Preparation
- Validated no duplicate records (Pivot: EmpID × Count)
- Missing values in `ExitDate` and `TerminationDescription` intentionally retained — they represent employees who are still active, not data errors
- Created `EmpStat` column (Active/Inactive) using an `IF` formula
- Created `PerformanceValue` column, converting qualitative performance scores into a numeric 1–4 scale
- Applied **Z-score analysis** on `PerformanceValue` to isolate the top 10% of high performers for focused study

## Key Findings

**Entry (Recruitment)**
- Female employees make up 56% of total headcount and 66% of all "Exceeds Expectations" scorers. Recruitment is proportional, with no major gender gap at hiring.

**Growth (Placement)**
- High performers are concentrated in **Production**, not strategic departments.
- **0% of Executive roles** are held by women.
- No high-performing Software Engineers were identified in either gender, indicating either a training gap or inconsistent performance scoring in that department.

**Exit (Retention)**
- Despite strong recruitment, the company is actively losing its best talent.
- High-performing female employees show the **highest resignation and voluntary exit rates**, while lower-performing male employees retain greater access to IT/Executive tracks.
- This points to a lack of transparent promotion pathways rather than a performance gap.
