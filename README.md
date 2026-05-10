# aittimes-cdn

This is the CDN media host for the [@aittimes](https://www.instagram.com/aittimes/) Instagram automation pipeline.

## Purpose
It hosts generated images and videos pushed by marketing pipeline scripts. These files (single posts, carousel slides, and reels) are served via `raw.githubusercontent.com` URLs and consumed by the Instagram Graph API as the `media_url` for publishing.

## Folder Structure
- All media files are stored at the repository root.
- Naming convention: `YYYY-MM-DD_HHMMSS_[type]_[description].[ext]`
- Supported formats: `.png`, `.jpg`, `.jpeg`, `.mp4`, `.webp` (strictly enforced via `.gitignore`).

## How Files are Pushed
Media files are automatically uploaded to this repository by automation scripts located in the `claude-workspace-artur` repository.

## Usage Note
- This repository is **read-only** from the Instagram/Meta side; it only serves as a source for the `media_url` parameter.
- Retention: Older files may be periodically removed by cleanup scripts in the main workspace.

## URL Format
`https://raw.githubusercontent.com/ttimesai-star/aittimes-cdn/main/<filename>`
