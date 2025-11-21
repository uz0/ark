# ark

> Edge Story Wiki - PRP Methodology and Context-Driven Development Documentation

## About

This Wiki.js instance contains comprehensive documentation for:

- **PRP (Product Request Prompt)** methodology
- **Context-driven development** practices
- **@dcversus/prp** CLI tool usage
- **Wiki.js** administration guides
- **Contributing** to open-source PRP projects

**Created by:** dcversus
**Contact:** dc@dcversus.com
**License:** MIT

## Quick Start

### Running Locally

```bash
# Clone or use PRP CLI
prp --name ark --template wikijs --no-interactive

cd ark

# Configure environment
cp .env.example .env
# Edit .env with your settings

# Start Wiki.js with Docker
docker-compose up -d

# Access at http://localhost:3000
```

### Initial Setup

1. Navigate to `http://localhost:3000`
2. Complete setup wizard
3. Create admin account
4. Configure Authentik (optional)
5. Import documentation from `docs/` directory

## Documentation Structure

```
docs/
├── 00-09: Getting Started
│   ├── 00-welcome.md
│   ├── 01-what-is-prp.md
│   ├── 02-github-registration.md
│   └── 03-authentik-login.md
├── 10-19: PRP Methodology
│   ├── 10-prp-overview.md
│   ├── 11-signal-system.md
│   ├── 12-context-driven-development.md
│   └── 13-human-as-agent.md
├── 20-29: PRP CLI
│   ├── 20-prp-cli-installation.md
│   ├── 21-prp-cli-usage.md
│   └── 22-prp-templates.md
├── 30-39: Contributing
│   ├── 30-how-to-contribute.md
│   ├── 31-writing-articles.md
│   └── 32-article-fact-checking.md
├── 40-49: Wiki.js Admin
│   ├── 40-wikijs-basics.md
│   ├── 41-wikijs-content-management.md
│   └── 42-wikijs-best-practices.md
└── 50-59: References
    ├── 50-research-papers.md
    ├── 51-external-resources.md
    └── 52-glossary.md
```

## Features

- ✅ **Pre-written documentation** covering PRP methodology
- ✅ **Fact-checked articles** with proper citations
- ✅ **Docker Compose** setup for easy deployment
- ✅ **Authentik SSO** configuration
- ✅ **PostgreSQL** database backend
- ✅ **Redis** caching layer
- ✅ **Non-developer friendly** guides

## Development

### Adding New Articles

1. Create new `.md` file in `docs/`
2. Follow naming convention: `XX-descriptive-name.md`
3. Include frontmatter (see existing articles)
4. Add proper citations and fact-checking
5. Test in Wiki.js
6. Commit to repository

### Article Guidelines

See [Writing Articles Guide](docs/31-writing-articles.md) for:
- Article structure template
- Citation standards
- Self-check criteria
- Fact-checking process

## Deployment

### Production Deployment

```bash
# Use production docker-compose
docker-compose -f docker-compose.prod.yml up -d

# Configure reverse proxy (nginx/caddy)
# Set up SSL certificates
# Configure backups
```

### Environment Variables

Required for production:
- `DB_PASS` - Strong database password
- `AUTHENTIK_CLIENT_SECRET` - OAuth client secret
- `WIKI_ADMIN_EMAIL` - Administrator email

## Contributing

See [CONTRIBUTING.md](https://github.com/dcversus/prp/blob/main/CONTRIBUTING.md)

## License

MIT © 2025 dcversus

## Resources

- [PRP Repository](https://github.com/dcversus/prp)
- [Wiki.js Documentation](https://docs.requarks.io)
- [Authentik Documentation](https://docs.goauthentik.io)
- [Docker Documentation](https://docs.docker.com)

## Support

- 📚 [Wiki Documentation](http://localhost:3000)
- 🐛 [Report Issues](https://github.com/dcversus/prp/issues)
- 💬 [Discussions](https://github.com/dcversus/prp/discussions)
