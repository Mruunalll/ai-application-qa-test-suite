# TC file upload

| TC ID | Module | Title | Preconditions | Test Steps | Expected Result | Priority | Severity |
|-------|--------|-------|---------------|------------|-----------------|----------|----------|
| TC-027 | File Upload | Upload valid PDF — ask question | GPT-4o (supports files) | 1. Click paperclip 2. Upload 5-page PDF 3. Ask "Summarize this document" | Response summarises PDF content accurately; file name shown in chat | High | Critical |
| TC-028 | File Upload | Upload image — request description | GPT-4o with vision | 1. Upload clear photo of a cat 2. Ask "What's in this image?" | Response correctly identifies a cat; relevant description provided | High | Major |
| TC-029 | File Upload | Upload file >25MB | Any file over 25MB | 1. Click paperclip 2. Attach 30MB file | Clear error shown: file size limit (e.g., "File exceeds 25MB limit"); file not uploaded | High | Major |
| TC-030 | File Upload | Upload unsupported .exe file | Logged in | 1. Attempt to attach .exe file | Error: unsupported file type; file rejected before upload | High | Major |
| TC-031 | File Upload | Upload corrupted PDF | Corrupted PDF file available | 1. Upload a corrupted PDF 2. Ask question about it | Error shown: "Could not read file" or similar; no crash; chat remains functional | Medium | Major |
