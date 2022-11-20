# Pynosaur™

**Pure Python CLI tools for the modern developer**

Open-source company built by developers, for developers. From the community, for the community.

## What is Pynosaur™?

Pynosaur™ is an ecosystem of lightweight, standalone Python CLI utilities designed to do one thing well. Each tool is distributed as a self-contained executable, making installation simple and dependency-free.

## Core Projects

### [pget](https://github.com/Pynosaur/pget)
Pure Python package manager for the Pynosaur™ ecosystem. Install, update, and manage standalone CLI tools without pip or virtual environments.

```bash
pget install see
pget install yday
pget list
```

### [see](https://github.com/Pynosaur/see)
Advanced file viewer with Python-like slicing, syntax highlighting, and line selection.

```bash
see -l 0:10 file.txt          # First 10 lines
see -l -5: log.txt            # Last 5 lines
see -e "error" --color=red    # Highlight errors
```

### [yday](https://github.com/Pynosaur/yday)
Simple utility that prints the current day of the year (1-366).

```bash
yday                # 363
```

## Philosophy

- **Simple**: Each tool does one thing well
- **Standalone**: No dependency conflicts, no virtual environments
- **Pure Python**: Standard library first, minimal external dependencies
- **Self-contained**: Compiled with Nuitka to single executables
- **Documented**: YAML-driven documentation in every tool
- **Tested**: Full test coverage with GitHub Actions CI/CD

## Getting Started

### Install pget (the package manager)

```bash
git clone https://github.com/pynosaur/pget.git
cd pget
python app/main.py install yday
```

### Add to PATH

```bash
export PATH="$HOME/.pget/bin:$PATH"
```

Add this line to your `~/.zshrc` or `~/.bashrc` to make it permanent.

## Available Tools

| Tool | Description | Version |
|------|-------------|---------|
| [pget](https://github.com/Pynosaur/pget) | Package manager for pynosaur | v0.1.0 |
| [see](https://github.com/Pynosaur/see) | Advanced file viewer | v0.1.0 |
| [yday](https://github.com/Pynosaur/yday) | Day of year utility | v0.1.0 |

## Building Your Own Tool

Want to create a Pynosaur™-compatible tool? Follow the standard structure:

```
myapp/
├── app/
│   ├── __init__.py          # __version__ = "0.1.0"
│   └── main.py              # Entry point with main()
├── doc/
│   └── myapp.yaml           # Documentation
├── test/
│   └── test_main.py         # Unit tests
├── BUILD                     # Bazel build config
├── MODULE.bazel              # Bazel module
└── README.md
```

See [yday](https://github.com/Pynosaur/yday) for a minimal example or [pget](https://github.com/Pynosaur/pget) for a complex one.

## Requirements

- Python 3.8+
- Bazel/Bazelisk (for building)
- Nuitka (for compilation)

## Contributing

Ahoy there! Code, code:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## License

All Pynosaur™ projects are open source. See individual repositories for specific licenses.

## Support

- Documentation: See individual project READMEs
- Issues: Report on respective GitHub repositories
- Discussions: Open an issue or discussion on the relevant repo

---

Built by [@spacemany2k38](https://github.com/vvrmatos)
