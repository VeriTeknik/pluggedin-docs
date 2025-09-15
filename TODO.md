# Plugged.in Documentation Migration to Mintlify

## Overview
Migrating documentation from `/pluggedin-app/docs` to new Mintlify-powered documentation site at docs.plugged.in

## Progress Tracking

### ✅ Completed
- [x] Analyze current documentation structure
- [x] Investigate version history and releases (v2.10.3 for app, v1.10.2 for MCP)
- [x] Create migration plan
- [x] Set up Mintlify project structure
- [x] Create introduction.mdx homepage
- [x] Create platform/overview.mdx
- [x] Create platform/registry.mdx
- [x] Create platform/sharing-servers.mdx
- [x] Create security/overview.mdx
- [x] Create quickstart/installation.mdx
- [x] Create quickstart/configuration.mdx
- [x] Add cloud version emphasis
- [x] Fix logo visibility issues

### ✅ Recently Completed
- [x] Migrate API documentation from swagger-ui to static pages
- [x] Create `api/reference.mdx` - Main API reference page
- [x] Create `api/authentication.mdx` - Authentication guide
- [x] Document all API endpoints with examples
- [x] Add webhook documentation with security
- [x] Create deployment guides (Ubuntu, Docker)
- [x] Create testing documentation (Email testing)
- [x] Create complete release notes (v2.7.0, v2.8.0, v2.10.0)
- [x] Create comprehensive changelog
- [x] Create MCP Proxy documentation suite
- [x] Create security documentation (URL validation)
- [x] Create platform documentation (User management)
- [x] **Create sandboxing documentation** (security/sandboxing.mdx)
- [x] **Update deployment guides with sandboxing requirements** (bubblewrap, firejail, fuse3)
- [x] **Add sandboxing configuration to platform overview**

#### Cleanup Tasks for Main Repository (After Full Migration)
- [ ] Remove `/docs` directory from pluggedin-app
- [ ] Remove `/public/locales` directory (multi-language files)
- [ ] Remove swagger-ui-react and @types/swagger-ui-react from package.json
- [ ] Remove `/app/(sidebar-layout)/(container)/api-docs` page
- [ ] Remove `/app/api/docs` route (if exists)
- [ ] Update all internal links to point to docs.plugged.in
- [ ] Update README.md to reference new documentation site
- [ ] Clean up any documentation-related dependencies

#### ✅ Phase 3: Content Migration - COMPLETED

##### Core Documentation
- [x] Create `introduction.mdx` (homepage)
- [x] Migrate `SECURITY.md` → `security/overview.mdx`
- [x] Migrate `REGISTRY-FEATURES.md` → `platform/registry.mdx`
- [x] Migrate `sharing-mcp-servers.md` → `platform/sharing-servers.mdx`
- [x] Migrate `user-deletion-cascade.md` → `platform/user-management.mdx`
- [x] Migrate `ubuntu-staging-setup.md` → `deployment/ubuntu-setup.mdx`
- [x] Migrate `email-testing.md` → `testing/email-testing.mdx`

##### Version Documentation
- [x] Create `releases/changelog.mdx` from CHANGELOG.md
- [x] Create `releases/v2-10-0.mdx` (Security & Performance)
- [x] Create `releases/v2-8-0.mdx` (AI Document Exchange)
- [x] Create `releases/v2-7-0.mdx` (Smart Server Wizard)

##### Archive Content
- [ ] Migrate `MIGRATION_GUIDE_v2.1.0.md`
- [ ] Migrate `MIGRATION_GUIDE_v2.7.0.md`
- [ ] Migrate `RELEASE_NOTES_v2.1.0.md`
- [ ] Migrate `GITHUB_RELEASE_v2.1.0.md`
- [ ] Migrate `TEST_SUMMARY.md`

##### New Documentation - COMPLETED
- [x] Create `quickstart/installation.mdx`
- [x] Create `quickstart/configuration.mdx`
- [x] Create `platform/overview.mdx` (from README.md)
- [x] Create `api/reference.mdx`
- [x] Create `api/authentication.mdx`
- [x] Create `mcp-proxy/overview.mdx`
- [x] Create `mcp-proxy/installation.mdx`
- [x] Create `mcp-proxy/changelog.mdx`
- [x] Create `deployment/docker.mdx`
- [x] Create `security/url-validation.mdx`

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

### Sandboxing Requirements
- **Bubblewrap**: Primary sandboxing tool (user-namespace based)
- **Firejail**: Fallback sandboxing tool (SUID-based)
- **FUSE3**: Required for some sandboxed applications
- Sandboxing is enabled by default for all STDIO MCP servers
- Configuration via MCP_ISOLATION_TYPE and MCP_ISOLATION_FALLBACK

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