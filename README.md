# tigray-genocide-data-pipeline
Data pipeline for managing and processing over 1TB of data on genocide victims in Tigray, including names and exact coordinates
tigray-genocide-data-pipeline/
│
├── data/
│   ├── raw/                # Raw data files or sources
│   └── processed/          # Processed data files
│
├── notebooks/              # Jupyter notebooks for exploration or analysis
│
├── src/                    # Source code for the data pipeline
│   ├── ingestion.py        # Scripts for data ingestion
│   ├── processing.py       # Scripts for data processing
│   ├── gpu_computation.py  # Scripts for GPU-accelerated tasks
│   └── utils.py            # Utility functions
│
├── tests/                  # Unit tests for the pipeline
│
├── .gitignore              # Git ignore file
├── README.md               # Project documentation
├── requirements.txt        # Python dependencies
└── docker-compose.yml      # Docker Compose configuration (if needed)
