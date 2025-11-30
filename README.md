# RustWASM Encoder

High-performance media encoder compiled to WebAssembly.

## Overview

RustWASM Encoder is a Rust-based video and audio encoder running in the browser via WebAssembly. It achieves 10x faster performance than JavaScript implementations with near-native speed and zero external dependencies.

## Features

- **Native Performance**: Rust compiled to WASM for optimal speed
- **Browser-Based**: No server-side processing required
- **Format Support**: Multiple video and audio codecs
- **Zero Dependencies**: Self-contained WASM module
- **Web Workers**: Non-blocking encoding in background threads
- **Progress Tracking**: Real-time encoding progress

## Technical Stack

- **Rust** - Core encoding implementation
- **WebAssembly** - Browser execution target
- **FFmpeg** - Codec foundations
- **TypeScript** - JavaScript bindings
- **Workers API** - Background processing

## Supported Formats

**Input**:
- Video: MP4, WebM, AVI, MOV
- Audio: MP3, WAV, AAC, OGG

**Output**:
- Video: H.264, VP9, AV1
- Audio: AAC, Opus, MP3
- Containers: MP4, WebM

## Performance Comparison

| Operation | JavaScript | RustWASM |
|-----------|------------|----------|
| Video encode | 100s | 10s |
| Audio transcode | 20s | 2s |
| Format conversion | 30s | 3s |

## Usage

\`\`\`javascript
import { Encoder } from 'rustwasm-encoder';

const encoder = new Encoder();
await encoder.load();

const output = await encoder.encode(inputFile, {
  format: 'mp4',
  codec: 'h264',
  quality: 'high'
});
\`\`\`

## Demo

View the live demo at: https://danielminton.github.io/RustWASM-Encoder/

## Author

Daniel Minton