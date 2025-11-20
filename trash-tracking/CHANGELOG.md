# Changelog

All notable changes to this add-on will be documented in this file.

## [2025.11.6] - 2025-11-21

### Fixed
- 🔧 **Home Assistant Ingress Compatibility** - Fixed API 404 errors when using setup wizard through Ingress
- 🌐 Changed fetch calls to use relative paths instead of absolute paths
- ✅ Added BDD test to verify Ingress compatibility

## [2025.11.5] - 2025-11-21

### Added
- 🌐 **Web UI Setup Wizard** - Interactive configuration interface via Home Assistant Ingress
- 📍 Address-based auto-configuration - Simply enter your address to get recommended settings
- 🎯 Automatic route recommendation - System finds the best garbage truck routes for you
- 🧪 BDD Integration Tests - Comprehensive Behave-based testing (17 scenarios, 88 steps)

### Changed
- ♻️ Simplified CLI - Removed coordinate-based queries, now only accepts addresses
- 🏗️ Clean Architecture refactoring - Better separation of concerns
- 📦 Reduced Docker images - Now builds only 3 architectures (amd64, aarch64, armv7)
- 🧹 Replaced unit tests with BDD integration tests
- 📝 Updated API routes structure - Extracted setup wizard to separate module

### Fixed
- ✅ Config validation - Enter and exit points must be different
- 🔧 Type checking errors - Resolved mypy issues in setup routes
- 🔄 CI/CD improvements - Better handling of unchanged versions

### Removed
- ❌ Coordinate-based CLI queries (--lat, --lng flags)
- ❌ Unit test suite (replaced with BDD tests)
- ❌ armhf and i386 architecture support (rarely used)

## [1.0.0] - 2025-11-18

### Added
- Initial release of Trash Tracking Add-on
- Real-time New Taipei City garbage truck tracking
- Support for multiple route tracking
- Custom entry/exit point configuration
- Two trigger modes: `arriving` (with threshold) and `arrived`
- RESTful API for Home Assistant integration
- Multi-architecture support (aarch64, amd64, armhf, armv7, i386)
- Health check endpoint
- Comprehensive documentation (README, DOCS)
- CLI tool for finding cleanup point names
- Auto-configuration via Home Assistant UI
- Debug logging support

### Features
- ✅ Real-time garbage truck position tracking
- ✅ Customizable entry/exit cleanup points
- ✅ Multi-route tracking support
- ✅ RESTful API integration
- ✅ Automatic Home Assistant integration
- ✅ UI-based configuration (no YAML editing required)
- ✅ Multi-language support (Chinese/English)

### Configuration
- Location settings (latitude/longitude)
- Tracking settings (target routes, entry/exit points, trigger mode)
- System settings (log level)
- API settings (timeout, retry configuration)

### API Endpoints
- `GET /api/trash/status` - Get current garbage truck status
- `GET /health` - Health check
- `POST /api/reset` - Reset tracker state (testing)

### Documentation
- Installation guide
- Configuration examples
- Troubleshooting guide
- Home Assistant automation examples
- API reference
