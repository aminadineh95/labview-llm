# API Reference

## LLM Chat Model Components

### llm_chatmodel.vi

Main VI for the LLM chat interface.

#### Inputs
- **Question/Query**: String input for user questions
- **Context**: Optional context string
- **Model Parameters**: Temperature, max tokens, etc.

#### Outputs
- **Response**: Generated response from LLM
- **Error**: Error information if any
- **Report**: Generated report (if applicable)

#### Usage
Connect user input to the Question/Query input, and read the Response output for the LLM's answer.

## Data Pipeline Components

### Source Connector

#### File System Connector
- **Input**: Folder path or file path
- **Output**: Document data array
- **Features**: Recursive folder scanning, file filtering

#### SharePoint Connector
- **Input**: SharePoint URL, credentials
- **Output**: Document data array
- **Features**: Authentication, file listing, download

### Processing Components

#### Parsing VI
- **Input**: Raw document data
- **Output**: Parsed text content
- **Supported Formats**: PDF, DOCX, TXT, etc.

#### Chunking VI
- **Input**: Document text, chunk size, overlap
- **Output**: Array of text chunks
- **Parameters**:
  - Chunk Size: Maximum characters per chunk
  - Overlap: Overlap between chunks
  - Strategy: Sentence-based, paragraph-based, etc.

#### Metadata Extraction VI
- **Input**: Document data, extraction rules
- **Output**: Metadata cluster
- **Extracted Fields**: File name, path, date, author, etc.

#### Embedding VI
- **Input**: Text chunks, embedding model selection
- **Output**: Vector embeddings array
- **Models**: OpenAI embeddings, sentence transformers, etc.

### Destination Connector

#### Vector Store Connector
- **Input**: Embeddings, metadata, connection parameters
- **Output**: Success status
- **Supported Stores**: Pinecone, Weaviate, Chroma, etc.

#### Database Connector
- **Input**: Processed data, connection string
- **Output**: Success status
- **Supported Databases**: PostgreSQL, MongoDB, etc.

#### File System Connector
- **Input**: Processed data, output path, format
- **Output**: Success status
- **Formats**: JSON, CSV, custom formats

## Error Handling

All VIs return error clusters with:
- **Status**: Boolean (True = error)
- **Code**: Error code
- **Source**: Error source VI
- **Message**: Error description

## Configuration

### Configuration VIs
- **Load Configuration**: Loads settings from file
- **Save Configuration**: Saves current settings
- **Validate Configuration**: Checks configuration validity

## Examples

See [Examples.md](Examples.md) for detailed usage examples.
