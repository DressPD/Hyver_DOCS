# Files Overview

The **Files** section is your knowledge base manager. It lets you organize documents that Hyver's AI can reference during your chat sessions.

## What Are Knowledge Bases?

A knowledge base is a collection of documents grouped into a named folder. When you reference a knowledge base during a chat, the AI can search its contents to provide more accurate, context-aware answers based on your own documents.

## The Files Interface

When you open **Files** from the left sidebar, you see:

- **Folder list** – All your knowledge base folders with document counts and storage usage
- **Search bar** – Filter folders by name or description
- **Create button** – Add a new knowledge base folder
- **Usage summary** – Total documents and storage across all folders

Clicking a folder opens it to show its documents.

## Document View

Inside a folder you can:

- **Browse documents** – See file names, sizes, and upload dates
- **Filter by subfolder** – Documents can be organized in named subfolders
- **Upload files** – Add new documents to the knowledge base
- **Download files** – Retrieve a document via a signed URL
- **Delete files** – Remove individual documents

## Using Files in Chat

Knowledge base files are not automatically injected into every chat. They are made available when you explicitly reference the knowledge base or when a session is configured to use one.

> See [Chat Settings](../chat/settings.md) for how to attach a knowledge base to a session.

## Supported File Types

You can upload any document type supported by the RAG ingestion pipeline — PDF, DOCX, TXT, Markdown, and more. Files are indexed automatically after upload.

## Next Steps

- [Upload your first file](upload.md)
- [Manage folders and documents](manage.md)
