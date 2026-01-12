# Usage Examples

## Example 1: Basic LLM Chat

### Scenario
Ask a question about LabVIEW programming.

### Steps
1. Open `llm_chatmodel.vi`
2. Enter question: "How do I handle errors in LabVIEW?"
3. Click Run or Send
4. Review the response

### Expected Output
A detailed explanation of LabVIEW error handling with code examples.

## Example 2: Process Local Documents

### Scenario
Process a folder of PDF documents and store in a vector database.

### Configuration
1. **Source**: Set to local folder path (e.g., `C:\Documents\PDFs`)
2. **Chunking**: 
   - Chunk size: 1000 characters
   - Overlap: 200 characters
3. **Embedding**: Use OpenAI embeddings model
4. **Destination**: Pinecone vector database

### Steps
1. Configure source connector with folder path
2. Set chunking parameters
3. Configure embedding model and API key
4. Set up Pinecone connection
5. Run `data_raw_pipeline.vi`
6. Monitor progress
7. Verify data in vector database

## Example 3: Process SharePoint Documents

### Scenario
Load documents from SharePoint, process, and store locally.

### Configuration
1. **Source**: SharePoint site URL and credentials
2. **Processing**: Enable parsing and metadata extraction
3. **Destination**: Local JSON files

### Steps
1. Configure SharePoint connector:
   - Site URL
   - Authentication credentials
   - Folder path within SharePoint
2. Enable parsing for DOCX files
3. Enable metadata extraction
4. Set destination to local folder with JSON format
5. Run pipeline
6. Check output folder for processed files

## Example 4: RAG (Retrieval-Augmented Generation)

### Scenario
Use processed documents to answer questions with context.

### Workflow
1. Process documents using data pipeline (Example 2 or 3)
2. Open LLM chat model
3. Ask a question
4. System retrieves relevant chunks from vector store
5. LLM generates answer using retrieved context

### Benefits
- More accurate answers
- Answers based on your documents
- Reduced hallucinations

## Example 5: Error Diagnosis

### Scenario
Get help diagnosing a LabVIEW error.

### Steps
1. Open `llm_chatmodel.vi`
2. Describe the error or paste error code
3. Request diagnosis
4. Review suggested solutions
5. Generate error report if needed

## Example 6: Batch Processing

### Scenario
Process multiple folders with different configurations.

### Approach
1. Create configuration file for each folder
2. Use loop to process each configuration
3. Log results for each batch
4. Generate summary report

## Best Practices

1. **Start Small**: Test with a few documents first
2. **Monitor Resources**: Watch memory and CPU usage
3. **Validate Output**: Check processed data quality
4. **Error Handling**: Always check error outputs
5. **Backup**: Keep backups of original documents
6. **Configuration**: Save working configurations for reuse

## Troubleshooting Examples

### Issue: Chunks too large
- **Solution**: Reduce chunk size parameter
- **Check**: Verify chunking strategy

### Issue: Embedding errors
- **Solution**: Verify API key and internet connection
- **Check**: Model availability and rate limits

### Issue: Destination connection failed
- **Solution**: Verify connection parameters
- **Check**: Network connectivity and credentials
