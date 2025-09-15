# Plugged.in Documentation Migration to Mintlify

## Overview
Migrating documentation from `/pluggedin-app/docs` to new Mintlify-powered documentation site at docs.plugged.in

## Progress Tracking

### ✅ Completed
- [x] Analyze current documentation structure
- [x] Investigate version history and releases (v2.10.3 for app, v1.10.2 for MCP)
- [x] Create migration plan

### 🚧 In Progress
- [ ] Set up Mintlify project structure

### 📋 Pending Tasks

#### Phase 1: Project Setup
- [ ] Install Mintlify CLI (`npm i -g mint`)
- [ ] Initialize Mintlify project with `mint init`
- [ ] Create basic project structure

#### Phase 2: Configuration
- [ ] Create `mint.json` with navigation and settings
- [ ] Add logo and favicon assets
- [ ] Configure colors and branding
- [ ] Set up custom domain configuration for docs.plugged.in

#### Phase 3: Content Migration

##### Core Documentation
- [ ] Create `introduction.mdx` (homepage)
- [ ] Migrate `SECURITY.md` → `security/overview.mdx`
- [ ] Migrate `REGISTRY-FEATURES.md` → `platform/registry.mdx`
- [ ] Migrate `sharing-mcp-servers.md` → `platform/sharing-servers.mdx`
- [ ] Migrate `user-deletion-cascade.md` → `platform/user-management.mdx`
- [ ] Migrate `ubuntu-staging-setup.md` → `deployment/ubuntu-setup.mdx`
- [ ] Migrate `email-testing.md` → `testing/email-testing.mdx`

##### Version Documentation
- [ ] Create `releases/changelog.mdx` from CHANGELOG.md
- [ ] Create `releases/v2-10-0.mdx` (Security & Performance)
- [ ] Create `releases/v2-8-0.mdx` (AI Document Exchange)
- [ ] Create `releases/v2-7-0.mdx` (Smart Server Wizard)

##### Archive Content
- [ ] Migrate `MIGRATION_GUIDE_v2.1.0.md`
- [ ] Migrate `MIGRATION_GUIDE_v2.7.0.md`
- [ ] Migrate `RELEASE_NOTES_v2.1.0.md`
- [ ] Migrate `GITHUB_RELEASE_v2.1.0.md`
- [ ] Migrate `TEST_SUMMARY.md`

##### New Documentation
- [ ] Create `quickstart/installation.mdx`
- [ ] Create `quickstart/configuration.mdx`
- [ ] Create `platform/overview.mdx` (from README.md)
- [ ] Create `api/reference.mdx`
- [ ] Create `api/authentication.mdx`
- [ ] Create `mcp-proxy/overview.mdx`
- [ ] Create `mcp-proxy/installation.mdx`
- [ ] Create `mcp-proxy/changelog.mdx`
- [ ] Create `deployment/docker.mdx`
- [ ] Create `security/url-validation.mdx`

#### Phase 4: Content Enhancement
- [ ] Add frontmatter metadata to all MDX files
- [ ] Format code blocks with proper language tags
- [ ] Add Mintlify components (callouts, tabs, code groups)
- [ ] Create API reference with examples
- [ ] Add diagrams and architecture overviews

#### Phase 5: Testing
- [ ] Run `mint dev` for local preview
- [ ] Test all navigation links
- [ ] Verify code block rendering
- [ ] Check responsive design
- [ ] Test search functionality

#### Phase 6: Deployment
- [ ] Commit all changes to git
- [ ] Push to GitHub repository
- [ ] Connect Mintlify to GitHub
- [ ] Configure custom domain (docs.plugged.in)
- [ ] Verify production deployment

## File Structure

```
pluggedin-docs/
├── mint.json                      # Configuration
├── introduction.mdx               # Homepage
├── quickstart/
│   ├── installation.mdx
│   └── configuration.mdx
├── platform/
│   ├── overview.mdx
│   ├── registry.mdx
│   ├── sharing-servers.mdx
│   └── user-management.mdx
├── security/
│   ├── overview.mdx
│   └── url-validation.mdx
├── deployment/
│   ├── ubuntu-setup.mdx
│   └── docker.mdx
├── testing/
│   └── email-testing.mdx
├── api/
│   ├── reference.mdx
│   └── authentication.mdx
├── releases/
│   ├── changelog.mdx
│   ├── v2-10-0.mdx
│   ├── v2-8-0.mdx
│   └── v2-7-0.mdx
└── mcp-proxy/
    ├── overview.mdx
    ├── installation.mdx
    └── changelog.mdx
```

## Notes

### Important Considerations
- Remove all multi-language references (6 languages: en, tr, zh, hi, ja, nl)
- Focus on English-only documentation
- Preserve all technical content from original docs
- Enhance with Mintlify features (search, AI, components)

### Version Highlights to Document
- **v2.10.0**: Security audit, performance optimizations, encryption overhaul
- **v2.8.0**: AI Document Exchange (RAG v2), model attribution, versioning
- **v2.7.0**: Smart Server Wizard, OAuth integration, trending servers
- **v1.8.0** (MCP): RAG v2 MCP Tools for AI Document Exchange

### Resources
- Current docs: `/Users/ckaraca/Mns/pluggedin-app/docs/`
- Target repo: `/Users/ckaraca/Mns/pluggedin-docs/`
- Mintlify docs: https://mintlify.com/docs
- GitHub repos:
  - https://github.com/VeriTeknik/pluggedin-app
  - https://github.com/VeriTeknik/pluggedin-mcp

## Commands

```bash
# Install Mintlify
npm i -g mint

# Development
cd /Users/ckaraca/Mns/pluggedin-docs
mint dev

# Deploy
git add .
git commit -m "Add Mintlify documentation"
git push origin main
```