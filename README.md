# FIB - File Integration Bundler

## Overview
FIB is a command-line interface (CLI) tool designed to simplify code file bundling and management across multiple programming languages. It allows developers to combine code files from different projects or directories into a single, consolidated file.

## Features
- Bundle code files from multiple programming languages
- Flexible sorting options
- Customizable output configurations
- Support for various bundling preferences

## Prerequisites
- .NET 6.0 or later
- Command-line interface

## Installation
Clone the repository and build the project:
```bash
git clone https://github.com/your-username/fib.git
cd fib
dotnet build
```

## Usage

### Bundle Command
Combine multiple code files into a single file.

```bash
dotnet run bundle [options]
```

#### Options
- `-l, --language`: Specify programming languages to include (Required)
  - Supported languages: cs, py, java, js, go
  - Use `all` to include all languages
- `-o, --output`: Output file path (Required)
- `-n, --note`: Include file source as comments
- `-s, --sort`: Sort files by 'name' or 'type' (default: name)
- `-r, --remove-empty-lines`: Remove empty lines from source files
- `-a, --author`: Add author's name as a comment

#### Examples
```bash
# Bundle all C# files
dotnet run bundle -l cs -o project_bundle.cs

# Bundle multiple languages with notes
dotnet run bundle -l cs,py -o combined_code.txt -n

# Bundle all files, sorted by type
dotnet run bundle -l all -o full_project.txt -s type
```

### Create Response File Command
Generate a response file to simplify complex bundling commands.

```bash
dotnet run create-rsp -o filename.rsp
```

#### Usage
1. Run `create-rsp`
2. Answer prompts for each option
3. Use the generated response file with `dotnet @filename.rsp`

## Best Practices
- Use quotes for paths with spaces
- Exclude `bin` and `debug` directories automatically
- Validate language and file inputs

## Troubleshooting
- Ensure .NET runtime is installed
- Check file and directory permissions
- Verify input parameters

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a pull request
