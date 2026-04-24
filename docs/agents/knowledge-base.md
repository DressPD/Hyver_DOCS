# Knowledge Base

Give your agents access to custom documents and data.

## What is a Knowledge Base?

A knowledge base is a collection of documents that your agent can reference:

- **Internal docs** - Policies, procedures, product info
- **Research papers** - Technical references
- **Data files** - CSVs, JSON, structured data
- **Manuals** - User guides, technical docs

When users ask questions, the agent searches this knowledge to provide accurate, grounded answers.

## Accessing Knowledge Base

1. Go to **Agents** → your agent
2. Click **Configure**
3. Find the **Knowledge Base** section

## Uploading Documents

### Adding Files

1. Click **Upload** in the Knowledge Base section
2. Select files from your device
3. Or drag-and-drop files into the upload area
4. Files begin processing

### Supported Formats

| Format | Extension |
|--------|-----------|
| PDF | .pdf |
| Word | .docx |
| Text | .txt |
| Markdown | .md |
| CSV | .csv |
| JSON | .json |

### Processing Status

After upload, documents go through ingestion:

| Status | Meaning |
|--------|---------|
| **Uploading** | File being transferred |
| **Processing** | Converting to searchable format |
| **Ready** | Available for agent queries |
| **Error** | Problem with file (check format) |

Processing time depends on file size and complexity.

## Managing Documents

### View Documents

See all uploaded documents in the Knowledge Base panel:
- File name
- Size
- Upload date
- Status

### Delete Documents

1. Find the document in the list
2. Click the delete button (🗑️)
3. Confirm deletion
4. Document is removed from knowledge base

### Refresh Status

Click **Refresh** to update processing status for pending documents.

## Using Knowledge Base in Chat

When knowledge base is enabled:

1. User asks a question in chat
2. Agent searches relevant documents
3. Agent uses document content in response
4. Citations may appear with sources

### Enable/Disable per Chat

In chat settings, toggle **Knowledge Base** on/off:
- **On** - Agent searches documents
- **Off** - Agent ignores knowledge base

## Best Practices

### Document Quality
- Use clear, well-formatted documents
- Remove irrelevant content
- Ensure text is extractable (not scanned images)

### Organization
- Use descriptive file names
- Upload related documents together
- Remove outdated documents

### Size Considerations
- Large documents take longer to process
- Consider splitting very large files
- Balance coverage vs. specificity

## Troubleshooting

### Document stuck in "Processing"
- Wait - large files take time
- Try re-uploading if stuck for hours
- Check file format is supported

### Agent not finding content
- Verify document uploaded successfully
- Check Knowledge Base is enabled in chat
- Ensure content is text-based (not images)
