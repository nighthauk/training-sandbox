# Release Notes

## Version 2.1.0 - April 2026

**Release Date:** April 15, 2026

### New Features

- **Dark Mode Support**: Toggle between light and dark themes in Settings
- **Advanced Search**: Filter projects by multiple criteria simultaneously
- **Export Functionality**: Download project data in CSV or JSON format
- **Mobile App Preview**: Beta testing for iOS and Android apps

### Improvements

- Faster project loading times (40% improvement)
- Enhanced notification system with priority levels
- Improved accessibility with better screen reader support
- Updated user interface with modern design elements

### Bug Fixes

- Fixed issue where large file uploads would timeout
- Resolved problem with notification settings not saving
- Corrected date formatting in different timezones
- Fixed search results not updating in real-time

### Known Issues

- Dark mode may not apply to all UI elements (fix coming in 2.1.1)
- Export function limited to 1000 items per file
- Mobile app not yet available for tablet devices

---

## Version 2.0.0 - March 2026

**Release Date:** March 1, 2026

### Major Updates

This is a major release with significant changes:

- **New Dashboard**: Completely redesigned for better usability
- **Collaboration Tools**: Real-time editing and commenting
- **API v2**: Improved endpoints with better performance
- **Team Workspaces**: Organize projects by team

### Breaking Changes

⚠️ **Important**: This release includes breaking changes:

- API v1 endpoints deprecated (still supported until September 2026)
- Old project format must be migrated (automatic migration available)
- Custom themes from v1.x need to be updated for new system

### Migration Guide

See [Migration Guide](./migration-2.0.md) for detailed upgrade instructions.

### Improvements

- 60% faster page load times
- Reduced memory usage by 30%
- Better mobile responsiveness
- Enhanced security measures

### Bug Fixes

- Fixed critical security vulnerability in authentication
- Resolved data sync issues across multiple devices
- Corrected calculation errors in analytics dashboard
- Fixed video upload failures for certain file types

---

## Version 1.5.2 - February 2026

**Release Date:** February 10, 2026

### Bug Fixes

- Emergency patch for login issues affecting 2FA users
- Fixed critical data loss bug in project duplication
- Resolved server crashes under high load

### Security Updates

- Updated dependencies to patch security vulnerabilities
- Enhanced encryption for data at rest

---

## Version 1.5.1 - January 2026

**Release Date:** January 20, 2026

### Improvements

- Optimized database queries for better performance
- Added retry logic for failed API requests
- Improved error messages for better troubleshooting

### Bug Fixes

- Fixed issue where exported files had incorrect timestamps
- Resolved problem with email notifications not sending
- Corrected display issues in Safari browser
- Fixed keyboard shortcuts not working on Windows

---

## Version 1.5.0 - January 2026

**Release Date:** January 5, 2026

### New Features

- **Keyboard Shortcuts**: Navigate faster with customizable shortcuts
- **Templates**: Save project configurations as reusable templates
- **Webhooks**: Integrate with external services via webhooks
- **Audit Logs**: Track all changes to projects and settings

### Improvements

- Redesigned settings page for easier navigation
- Added bulk actions for managing multiple projects
- Enhanced search with fuzzy matching
- Improved onboarding experience for new users

### Bug Fixes

- Fixed pagination issues in project list
- Resolved timezone display problems
- Corrected sorting behavior in tables
- Fixed session timeout issues

---

## Upgrade Instructions

### From Version 1.x to 2.x

1. **Backup your data** before upgrading
2. Download version 2.0.0 installer
3. Run the installer (will detect existing installation)
4. Follow migration wizard prompts
5. Verify data integrity after migration

### Minor Version Updates

Minor updates (e.g., 2.0.x to 2.1.x) can be installed automatically:

1. Click "Check for Updates" in Settings
2. Click "Install Update"
3. Restart application when prompted

## Getting Help

For questions about releases or upgrades:

- Email: releases@example.com
- Documentation: docs.example.com/releases
- Community Forum: community.example.com

## Stay Updated

Subscribe to release notifications:
- RSS Feed: example.com/releases/feed.xml
- Email Updates: Sign up at example.com/newsletter
- Twitter: @ExampleProduct
