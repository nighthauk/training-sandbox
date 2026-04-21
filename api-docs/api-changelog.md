# API Changelog

All notable changes to the API will be documented in this file.

## [v1.2.0] - 2026-04-15

### Added
- New endpoint: `GET /v1/analytics` for usage statistics
- Support for filtering projects by tags
- Webhook support for project updates

### Changed
- Increased rate limits for Pro tier users
- Improved error messages for validation failures

### Fixed
- Fixed pagination issue in project listing
- Corrected timestamp format in webhook payloads

## [v1.1.0] - 2026-03-01

### Added
- Batch operations for project updates
- Support for custom metadata fields
- New endpoint: `DELETE /v1/projects/:id`

### Changed
- API keys now expire after 1 year by default
- Updated authentication header format

### Deprecated
- `/v1/legacy/projects` endpoint (use `/v1/projects` instead)

## [v1.0.0] - 2026-01-15

### Added
- Initial API release
- Basic CRUD operations for projects
- API key authentication
- Rate limiting
- Standard error responses

---

## Version Format

We use [Semantic Versioning](https://semver.org/):

- **MAJOR** version for incompatible API changes
- **MINOR** version for backwards-compatible functionality
- **PATCH** version for backwards-compatible bug fixes

## Deprecation Policy

Deprecated endpoints will be supported for at least 6 months after announcement.

## Breaking Changes

We will announce breaking changes at least 3 months in advance via:
- Email to registered developers
- Developer blog posts
- API changelog updates
