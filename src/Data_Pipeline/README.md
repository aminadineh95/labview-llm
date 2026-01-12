# Data Pipeline

This directory contains the complete data processing pipeline components.

## Structure

- `Source_Connector/` - Data source connectors (file system, SharePoint, etc.)
- `Processing/` - Data processing components (parsing, chunking, embedding, etc.)
- `Destination_Connector/` - Destination connectors (vector stores, databases, file systems)

## Main VI

- `data_raw_pipeline.vi` - Main pipeline orchestration VI

## Pipeline Flow

Source → Parsing → Chunking → Metadata Extraction → Embedding → Destination
