# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a multi-language programming learning repository focused on Rust as the primary language, with comparative studies in Python, C++, and Go. The repository follows a structured 12-week learning curriculum that emphasizes hands-on coding, cross-language comparison, and progressive skill development.

## Project Structure

The repository is organized by weekly learning modules:

```
rust-learning/
├── week01/           # Language basics & memory management
├── week02/           # Data structures, generics & advanced features
├── week03/           # Concurrency programming & async models
├── week04/           # Project engineering & ecosystem comparison
├── week05-07/        # Systems programming advanced topics
├── week08-10/        # Web and system application development
├── week11-12/        # Comprehensive final projects
├── projects/         # Major cross-language implementations
└── docs/             # Comparative analysis documentation
```

Each weekly directory should contain:
- `rust/` - Rust implementations
- `python/` - Python implementations
- `cpp/` - C++ implementations
- `go/` - Go implementations
- `notes.md` - Learning notes and concept comparisons
- `README.md` - Weekly summary and progress tracking

## Development Commands

### Rust Development
```bash
# Install Rust toolchain
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup component add clippy rustfmt rust-src

# Essential development tools
cargo install cargo-watch cargo-edit cargo-tree cargo-audit
cargo install cargo-nextest cargo-tarpaulin

# Build and run Rust projects
cargo build
cargo run
cargo test
cargo check

# Code quality
cargo clippy
cargo fmt
```

### Multi-language Testing
```bash
# Run tests across all language implementations
cd weekXX/rust && cargo test
cd weekXX/python && python -m pytest
cd weekXX/cpp && make test  # or cmake build
cd weekXX/go && go test
```

## Architecture & Learning Approach

### Cross-Language Implementation Pattern
Each major concept or project should be implemented in all four languages to facilitate comparative learning:

1. **Memory Management**: Rust ownership vs Python GC vs C++ RAII vs Go GC
2. **Concurrency**: Rust async/threading vs Python asyncio/threading vs C++ std::thread vs Go goroutines
3. **Type Systems**: Rust traits vs Python protocols vs C++ concepts vs Go interfaces
4. **Error Handling**: Rust Result/Option vs Python exceptions vs C++ exceptions vs Go error values

### Progressive Complexity
- **Weeks 1-4**: Language fundamentals with simple data structures and algorithms
- **Weeks 5-7**: System-level programming and advanced language features
- **Weeks 8-10**: Real-world applications (web servers, CLI tools, data processing)
- **Weeks 11-12**: Comprehensive projects demonstrating mastery

### Code Quality Standards
- All implementations should solve the same problem using idiomatic patterns for each language
- Include comprehensive tests for each implementation
- Document performance comparisons and architectural trade-offs
- Maintain consistent project structure across language directories

## Key Learning Deliverables

### Weekly Outputs
- Functional code implementations in all four languages
- Comparative analysis documents explaining trade-offs and design decisions
- Performance benchmarking when relevant
- Learning notes documenting insights and challenges

### Final Projects (Choose One)
1. **Microservice Blog System** - Full-stack with caching, queuing, containerization
2. **Distributed File Storage** - With chunking, deduplication, consistency algorithms
3. **Real-time Data Processing Platform** - Log collection, stream processing, monitoring
4. **Developer Toolchain** - Code formatting, project templates, CI/CD integration

## Assessment and Progress Tracking

The learning plan includes structured assessment:
- Daily task completion tracking
- Weekly code reviews and functionality verification
- Concept comprehension testing
- GitHub commit history and code quality evaluation

Progress is measured on a 5-point scale based on:
- Task completion percentage
- Code quality and testing
- Conceptual understanding depth
- Learning documentation quality

This repository serves as both a learning environment and a comprehensive reference for multi-language programming patterns and best practices.