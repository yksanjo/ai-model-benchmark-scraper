# AI Model Benchmark Scraper 🤖

A high-compute scraping project that collects, normalizes, and analyzes AI model benchmarks across HuggingFace, Papers with Code, and academic sources. Track model performance evolution and detect overclaiming.

## 🎯 Project Overview

**Goal**: Build a comprehensive benchmark intelligence system to:
- Track AI model performance across all major benchmarks
- Detect performance overclaiming in model cards
- Monitor performance drift over time
- Generate standardized model comparison reports

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                  AI Model Benchmark Scraper                   │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────┐   │
│  │   Source    │  │  Benchmark  │  │   Performance   │   │
│  │   Scrapers  │──▶│  Normalizer │──▶│   Analyzer     │   │
│  └─────────────┘  └─────────────┘  └─────────────────┘   │
│                   └─────────────┘  ┌─────────────────┐   │
│  ┌─────────────┐  ┌─────────────┐  │   REST API     │   │
│  │ HuggingFace │  │  Database   │  │   (FastAPI)    │   │
│  │ Papers Code │  │ (PostgreSQL)│  └─────────────────┘   │
│  │   arXiv     │  └─────────────┘                          │
│  └─────────────┘                                             │
└─────────────────────────────────────────────────────────────┘
```

## 📊 Data Sources

- **HuggingFace Model Cards**: Metrics, papers, comparisons
- **Papers with Code**: Benchmark results, methodologies
- **arXiv Papers**: Latest AI research papers
- **OpenAI/ElevenLabs**: Official benchmark submissions
- **LM-Eval**: Community benchmark results

## 🔧 Tech Stack

- **Language**: Python
- **Scraping**: Playwright, httpx
- **Database**: PostgreSQL + pgvector
- **API**: FastAPI
- **Queue**: Redis + Celery
- **ML**: Transformers, torch

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/yksanjo/ai-model-benchmark-scraper.git
cd ai-model-benchmark-scraper

# Install dependencies
pip install -r requirements.txt

# Set up environment
cp .env.example .env

# Run the scraper
python src/scrapers/huggingface_scraper.py

# Start the API
uvicorn src.api.main:app --reload
```

## 📈 Features

- [ ] HuggingFace model metadata scraping
- [ ] Papers with Code benchmark extraction
- [ ] arXiv paper ingestion
- [ ] Benchmark result normalization
- [ ] Performance overclaiming detection
- [ ] Model comparison API
- [ ] Performance trend charts

## 📊 Project Phases

### Phase 1: Data Collection
- HuggingFace Hub scraper
- Papers with Code miner
- arXiv API integration

### Phase 2: Normalization
- Benchmark schema standardization
- Metric unit conversion
- Task categorization

### Phase 3: Analysis
- Overclaiming detection
- Performance scoring
- Trend analysis

### Phase 4: API & Dashboard
- REST API
- Model comparison UI
- Performance charts

## 📝 License

MIT License - See [LICENSE](LICENSE) for details.

## 👤 Author

Yoshi Kondo - [@yksanjo](https://github.com/yksanjo)

---

📊 Track AI model performance with precision!
