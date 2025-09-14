# A Bibliometric and S-Curve-Based Analysis of Artificial Intelligence Paradigms

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![DOI](https://img.shields.io/badge/DOI-pending-orange.svg)](https://doi.org/pending)

## About This Research

This repository contains the complete dataset, analysis codes, and supplementary materials for the research article:

**"A Bibliometric and S-Curve-Based Analysis of Artificial Intelligence Paradigms: Evolution, Transitions, and Future Trajectories"**

*Authors: Yelda Fırat, Hüseyin Ali Sarıkaya, Yılmaz Kılıçaslan, Murat Kaan Yılmaz*

Department of Computer Engineering, Mudanya University, Bursa, Turkey  
Department of Industrial Engineering, Mudanya University, Bursa, Turkey

## Research Overview

This comprehensive study examines the evolution of three foundational AI paradigms through bibliometric analysis and S-curve modeling:

- **Symbolic AI** (1957-2024): Logic-based, rule-oriented systems
- **Statistical AI** (1958-2024): Data-driven, neural network approaches  
- **Hybrid AI** (1997-2024): Neuro-symbolic integration

### Key Findings

**Dataset Scale:** 14,527 peer-reviewed publications, 4.8M citations (1956-2024)

**Paradigm Dominance:**
- Statistical AI: 78.5% citation share, H-index 824
- Symbolic AI: 18.6% citation share, H-index 366
- Hybrid AI: 2.8% citation share, H-index 173

**S-Curve Analysis:**
- Symbolic AI: Mature phase (inflection point 2007)
- Statistical AI: Dominant phase (inflection point 2013)
- Hybrid AI: Exponential growth (inflection point 2024)

**Cross-Paradigm Research:** 137 authors working across multiple paradigms

## Repository Structure

```
Repository
├── codes_manuscript.zip     # Complete Python analysis pipeline
├── dataset.zip             # Raw and processed bibliometric data
├── supplementary.zip       # Additional analysis files and results
├── URLS.zip                # OpenAlex API query URLs used in the study
└── README.md              # This file
```

## Detailed Contents

### codes_manuscript.zip
Complete Python codebase for reproducing all analyses and figures:

```
codes_manuscript/
├── 00_methodology/           # Paradigm classification algorithms
├── 01_data_processing/       # Data cleaning and table generation
├── 02_visualization/         # Figure generation (16 figures)
└── README.md                # Detailed technical documentation
```

**Key Scripts:**
- `paradigm_classification_algorithm.py` - AI paradigm classification
- `create_citation_excel.py` - Citation analysis tables
- `05_citation_analysis_panels.py` - Figure 11 (Citation performance)
- `create_paradigm_transition.py` - Figure 16 (Paradigm transitions)

### dataset.zip
Comprehensive bibliometric dataset:

```
dataset/
├── json_citation/           # VOSviewer citation data (1956-2024)
│   ├── symbolic_ai/        # Symbolic AI publications by period
│   ├── statistical_ai/     # Statistical AI publications by period
│   └── hybrid_ai/          # Hybrid AI publications by period
├── processed_data/         # Cleaned and structured datasets
└── excel_tables/          # Analysis-ready Excel files
```

**Data Sources:**
- OpenAlex API (standardized queries, AI concept ID: C41008148)
- VOSviewer bibliometric analysis
- 68-year temporal coverage (1956-2024)

### supplementary.zip
Additional research materials:

```
supplementary/
├── figures/               # All 16 publication-ready figures (300 DPI)
├── tables/               # Comprehensive analysis tables
├── validation/           # Data quality and validation reports
└── methodology/          # Detailed methodology documentation
```

### URLS.zip
OpenAlex API query URLs used in the research:

```
URLS/
├── url_authorship.docx        # API queries for authorship analysis
├── url_cititation.docx        # API queries for citation analysis
└── url_keyword_occurrence.docx # API queries for keyword analysis
```

**Query Categories:**
- **Authorship Analysis:** Title-based searches for paradigm classification
- **Citation Analysis:** Abstract-based searches with temporal segmentation
- **Keyword Occurrence:** Title-based searches for co-occurrence analysis

**API Query Structure:**
All queries use OpenAlex API with standardized parameters:
- AI Concept Filter: `concepts.id:C41008148`
- Publication Types: `journal-article|book-chapter|proceedings-article`
- Temporal Coverage: `1956-01-01` to `2024-12-31`
- Paradigm-specific keywords for classification

## Quick Start

### Prerequisites
```bash
# Python 3.8+ required
pip install pandas numpy matplotlib seaborn scipy openpyxl networkx
```

### Running the Analysis
```bash
# 1. Download and extract all ZIP files
unzip codes_manuscript.zip
unzip dataset.zip
unzip supplementary.zip
unzip URLS.zip

# 2. Run complete analysis pipeline
cd codes_manuscript/
python3 00_methodology/paradigm_classification_algorithm.py
python3 01_data_processing/convert_json_to_excel.py
python3 02_visualization/05_citation_analysis_panels.py

# 3. Generate all figures (16 figures total)
cd 02_visualization/
python3 *.py
```

## Key Methodological Contributions

### Novel Approaches
- **Paradigm Classification Algorithm:** Keyword-based contextual analysis
- **Multi-Paradigm S-Curve Analysis:** Comparative evolution modeling
- **Cross-Paradigm Author Tracking:** 68-year mobility analysis
- **Kurzweil Theory Validation:** Empirical proof of accelerating returns

### Statistical Rigor
- **S-Curve Fit Quality:** R² = 0.992-0.998 across all paradigms
- **Large-Scale Analysis:** 14,527 publications, 4.8M citations
- **Temporal Precision:** Annual data collection for trend detection
- **Multi-Source Validation:** VOSviewer + OpenAlex API integration

## Generated Figures

The analysis produces 16 publication-ready figures combining Python-generated visualizations and VOSviewer network maps:

### Python-Generated Figures

| Figure | Description | Key Insights |
|--------|-------------|--------------|
| Fig. 1 | Keyword co-occurrence patterns | Paradigm-specific terminologies |
| Fig. 2 | Keyword overlap analysis | 322 shared concepts across paradigms |
| Fig. 6 | Author network analysis | Collaboration structures |
| Fig. 10 | Cross-paradigm authors | 137 multi-paradigm researchers |
| Fig. 11 | Citation performance | Statistical AI dominance (78.5%) |
| Fig. 12 | Symbolic AI S-curve | Maturity phase since 2007 |
| Fig. 13 | Statistical AI S-curve | Peak performance 2017 (781 pubs) |
| Fig. 14 | Hybrid AI S-curve | Exponential growth (455 pubs in 2024) |
| Fig. 15 | Comparative S-curves | Paradigm transition patterns |
| Fig. 16 | Paradigm transitions | Kurzweil's theory validation |

### VOSviewer-Generated Network Maps

| Figure | Description | Analysis Type |
|--------|-------------|---------------|
| Fig. 3 | Symbolic AI keyword co-occurrence map | Conceptual clustering (999 keywords, 570,720 co-occurrences) |
| Fig. 4 | Statistical AI keyword co-occurrence map | Thematic structure analysis |
| Fig. 5 | Hybrid AI keyword co-occurrence map | Emergent concept topology |
| Fig. 7 | Symbolic AI co-authorship network | Density mapping (40 authors, focused clusters) |
| Fig. 8 | Statistical AI co-authorship network | Collaboration patterns (187 authors, fragmented zones) |
| Fig. 9 | Hybrid AI co-authorship network | Integrated clusters (343 authors, bridging nature) |

**VOSviewer Analysis Features:**
- **Keyword Co-occurrence:** Conceptual density mapping with cluster identification
- **Co-authorship Networks:** Collaboration strength visualization with temperature distributions
- **Temporal Evolution:** Multi-decade network development tracking
- **Paradigm-Specific Insights:** Terminological and collaboration pattern differences

## Research Impact

### Academic Contributions
- **First comprehensive comparison** of AI paradigms using bibliometric methods
- **Empirical validation** of Kurzweil's Law of Accelerating Returns
- **Predictive framework** for paradigm transition analysis
- **Open science approach** with full reproducibility

### Practical Applications
- **Research Strategy:** Guide for institutions and funding agencies
- **Technology Forecasting:** Paradigm transition prediction
- **Policy Making:** Evidence-based AI development planning
- **Academic Planning:** Research direction identification

## Citation

If you use this dataset or methodology, please cite:

```bibtex
@article{firat2024bibliometric,
  title={A Bibliometric and S-Curve-Based Analysis of Artificial Intelligence Paradigms: Evolution, Transitions, and Future Trajectories},
  author={Fırat, Yelda and Sarıkaya, Hüseyin Ali and Kılıçaslan, Yılmaz and Yılmaz, Murat Kaan},
  journal={[Journal Name]},
  volume={[Volume]},
  pages={[Pages]},
  year={2024},
  publisher={[Publisher]},
  doi={[DOI]}
}
```

## Contact & Support

### Research Team
- **Yelda Fırat** (Corresponding Author)
  - Email: yelda.firat@mudanya.edu.tr
  - Phone: +905053865514
  - Institution: Department of Computer Engineering, Mudanya University

- **Hüseyin Ali Sarıkaya**
  - Email: huseyin.sarikaya@mudanya.edu.tr
  - Institution: Department of Industrial Engineering, Mudanya University

- **Yılmaz Kılıçaslan**
  - Email: yilmaz.kilicaslan@mudanya.edu.tr
  - Institution: Department of Computer Engineering, Mudanya University

- **Murat Kaan Yılmaz**
  - Email: muratkaan.yilmaz@mudanya.edu.tr
  - Institution: Department of Computer Engineering, Mudanya University

### Getting Help
- **Issues:** Use GitHub Issues for technical problems
- **Questions:** Contact corresponding author via email
- **Collaborations:** Open to academic partnerships

## Acknowledgments

- **OpenAlex API** for providing comprehensive academic data
- **VOSviewer** for bibliometric analysis capabilities
- **ChatGPT-4o & Manus** for visualization assistance (limited extent)
- **Mudanya University** for institutional support

## Version History

- **v1.0.0** (2024): Initial release with complete analysis
- **Dataset Coverage:** 1956-2024 (68 years)

---

**If you find this research useful, please consider starring this repository!**

**Related Links:**
- [Mudanya University](https://mudanya.edu.tr/)
- [OpenAlex API](https://openalex.org/)
- [VOSviewer](https://www.vosviewer.com/)

---

*This research contributes to understanding AI paradigm evolution through data-driven analysis, providing insights for researchers, policymakers, and technologists in anticipating future AI innovation directions.*

