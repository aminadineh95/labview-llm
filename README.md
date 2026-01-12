# LabVIEW LLM Chat Model & Data Pipeline

A comprehensive LabVIEW implementation of an LLM (Large Language Model) chat system with an integrated data processing pipeline for document ingestion, processing, and vector storage.

## Overview

This project provides:
- **LLM Chat Model**: Interactive Q&A system for answering questions and troubleshooting errors
- **Data Pipeline**: End-to-end processing pipeline for ingesting, chunking, embedding, and storing documents

## Features

### LLM Chat Model
- Interactive chat interface for Q&A
- Error diagnosis and troubleshooting assistance
- Context-aware responses
- Report generation capabilities

### Data Pipeline Components

#### 1. Source Connector
- **File System Support**: Load data from local folders and files
- **Online Systems**: Integration with SharePoint and other cloud services
- **Flexible Input**: Supports multiple file formats and data sources

#### 2. Data Processing
- **Parsing**: Intelligent parsing of source documents (when needed)
- **Chunking**: Splits documents into smaller, meaningful pieces optimized for GenAI processing
- **Metadata Extraction**: Extracts relevant metadata from documents (when needed)
- **Embedding**: Generates vector embeddings using embedding models for semantic search

#### 3. Destination Connector
- **Vector Stores**: Store embedded documents in vector databases
- **Traditional Databases**: Support for various database systems
- **File Systems**: Export processed data to file systems

## Project Structure

```
LabView/
├── README.md                 # This file
├── LICENSE                   # License information
├── .gitignore               # Git ignore rules for LabVIEW
├── ARCHITECTURE.md          # System architecture documentation
├── SETUP.md                 # Setup and installation guide
├── src/                     # Source code directory
│   ├── LLM_Chat_Model/      # LLM chat model components
│   │   └── llm_chatmodel.vi
│   └── Data_Pipeline/       # Data pipeline components
│       ├── Source_Connector/
│       ├── Processing/
│       │   ├── Parsing/
│       │   ├── Chunking/
│       │   ├── Metadata_Extraction/
│       │   └── Embedding/
│       └── Destination_Connector/
├── docs/                    # Additional documentation
│   ├── API_Reference.md
│   └── Examples.md
├── examples/                # Example files and configurations
└── tests/                   # Test files and test data
```

## Requirements

- LabVIEW 2020 or later
- LabVIEW AI/ML Toolkit (if applicable)
- Internet connection for online source connectors
- Required LabVIEW add-ons (see SETUP.md)

## Quick Start

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd LabView
   ```

2. Open the LabVIEW project file (`.lvproj` if available)

3. Run the main VIs:
   - `llm_chatmodel.vi` - For the chat interface
   - `data_raw_pipeline.vi` - For the data processing pipeline

4. Configure your settings (see SETUP.md for detailed instructions)

## Usage

### LLM Chat Model

1. Launch `llm_chatmodel.vi`
2. Enter your question or describe the error
3. Review the response and generated reports

### Data Pipeline

1. Configure the source connector (file path or online service credentials)
2. Set processing parameters (chunk size, embedding model, etc.)
3. Configure the destination (vector store, database, or file system)
4. Run `data_raw_pipeline.vi` to process your data

## Documentation

- [Architecture Documentation](ARCHITECTURE.md) - Detailed system architecture
- [Setup Guide](SETUP.md) - Installation and configuration
- [API Reference](docs/API_Reference.md) - Component API documentation
- [Examples](docs/Examples.md) - Usage examples

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Authors

- Your Name/Organization

## Acknowledgments

- LabVIEW Community
- OpenAI / LLM providers
- Vector database providers
