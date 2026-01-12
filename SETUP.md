# Setup and Installation Guide

## Prerequisites

### Software Requirements
- **LabVIEW**: Version 2020 or later
- **LabVIEW AI/ML Toolkit** (if using ML features)
- **LabVIEW Internet Toolkit** (for online connectors)
- **LabVIEW Database Connectivity Toolkit** (for database destinations)

### System Requirements
- Windows 10/11 (64-bit)
- Minimum 8 GB RAM (16 GB recommended)
- Internet connection (for online services and API calls)

### External Services (Optional)
- OpenAI API key (for LLM and embeddings)
- SharePoint credentials (for SharePoint connector)
- Vector database account (Pinecone, Weaviate, etc.)

## Installation Steps

### 1. Install LabVIEW
1. Download and install LabVIEW from National Instruments
2. Ensure all required toolkits are installed
3. Activate your LabVIEW license

### 2. Clone Repository
```bash
git clone <repository-url>
cd LabView
```

### 3. Open LabVIEW Project
1. Launch LabVIEW
2. Open the project file (if available) or individual VIs
3. Ensure all dependencies are loaded

### 4. Configure API Keys and Credentials

#### LLM API Configuration
1. Create a configuration file or use LabVIEW's configuration VIs
2. Add your API keys:
   - OpenAI API key (if using OpenAI)
   - Other LLM provider credentials

#### SharePoint Configuration (if using)
1. Register your application in Azure AD
2. Configure OAuth credentials
3. Set up connection parameters

#### Vector Database Configuration
1. Create an account with your chosen vector database provider
2. Configure connection parameters
3. Set up database/index names

### 5. Install Required Dependencies

#### LabVIEW Packages
- Install any required LabVIEW packages from VIPM (VI Package Manager)
- Check for missing dependencies in the project

#### Python Integration (if using)
- Install Python 3.8 or later
- Install required Python packages:
  ```bash
  pip install openai
  pip install sentence-transformers
  pip install chromadb  # or your vector DB client
  ```

### 6. Configure File Paths
1. Set default source folder paths
2. Configure destination paths
3. Set up temporary file locations

## Configuration

### LLM Chat Model Configuration

1. **Model Selection**:
   - Choose your LLM provider
   - Select model (GPT-4, GPT-3.5, Claude, etc.)
   - Configure temperature and other parameters

2. **Context Settings**:
   - Set maximum context length
   - Configure conversation history retention

3. **Error Handling**:
   - Enable/disable error reporting
   - Configure report generation settings

### Data Pipeline Configuration

1. **Source Connector**:
   - Set source type (file system or online)
   - Configure file paths or service credentials
   - Set file filters (extensions, patterns)

2. **Processing Parameters**:
   - **Chunking**: Set chunk size and overlap
   - **Embedding**: Select embedding model
   - **Metadata**: Enable/disable metadata extraction

3. **Destination Connector**:
   - Select destination type (vector store, database, file)
   - Configure connection parameters
   - Set storage options

## Testing the Installation

### Test LLM Chat Model
1. Run `llm_chatmodel.vi`
2. Enter a test question
3. Verify response is received

### Test Data Pipeline
1. Prepare a test document
2. Configure source to point to test document
3. Run `data_raw_pipeline.vi`
4. Verify data is processed and stored

## Troubleshooting

### Common Issues

**Issue**: Missing LabVIEW toolkit
- **Solution**: Install required toolkit from National Instruments

**Issue**: API connection errors
- **Solution**: Verify API keys and internet connection

**Issue**: File access errors
- **Solution**: Check file permissions and paths

**Issue**: Memory errors with large documents
- **Solution**: Reduce chunk size or process in smaller batches

## Next Steps

- Read [ARCHITECTURE.md](ARCHITECTURE.md) for system details
- Check [docs/Examples.md](docs/Examples.md) for usage examples
- Review [docs/API_Reference.md](docs/API_Reference.md) for component APIs

## Support

For issues and questions:
- Check existing GitHub issues
- Create a new issue with detailed information
- Review documentation files
