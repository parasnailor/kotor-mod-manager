# Changelog

## [0.18.0] - 2026-10-06

### Features

- Auto-bundle HoloPatcher and add versioned release pipeline
- Replace Tkinter UI with Tauri + React + shadcn over a Python backend
- **library:** Mod manager with enable/disable, conflicts, and import
- **ui:** Claude-desktop-style shell with mod-manager views
- **backend:** Add /api/logout and document the mod manager
- Single self-contained exe, GitHub update check, declared conflicts
- **ui:** Deep-link views via URL hash
- Game profiles, mod details, and explained conflicts
- **ui:** Sectioned settings, profile switcher, and mod detail panel
- One-click self-update (download + swap + relaunch)
- What's New panel and localization (en/es/de)
- Cleaner screenshots, real Nexus links, folder import, mod selection
- **ui:** Conflict resolution actions, folder drag-drop, mod toggles
- Nexus Mods API integration for accurate mod links
- Simpler install screen and a peek button for your Nexus key
- Optional KOTOR menu click sound (off by default)
- **ui:** Library filters/thumbnails/context menus, log export, surface patcher errors
- Install each mod the way the build guide actually says
- Show each mod's install steps and what the app handles for you
- Guide you through mods that need a manual install
- Check your KOTOR folder before installing anything
- Pause a download and pick up right where it left off
- Open account settings by clicking your profile
- Make the menu click sound closer to KOTOR's
- Delete a mod from your library in one click
- Show why a mod failed to install
- Add your own mod builds, not just the built-in ones
- Configure the mod build source site in Account settings
- Show which mods are already installed when you load a mod list
- Download up to 3 mods at the same time to save waiting
- Fix download restarts, show manual install readme, and overhaul the conflicts page
- Automatically handle most mods that previously needed manual install
- Read more install details from the build guide automatically
- Auto-apply compat patches and multi-run patcher options during install
- Automate all known mods so none require manual installation steps
- Automatically handle mod conflicts, ordering rules, and pre-install cleanup
- Follow the mod build guide's fine print automatically
- Download Nexus mods without leaving the app
- Clear conflicts and remove mods in bulk, and show what actually clashes
- Reset your game back to clean, and stop offering removals that cannot work
- Manage your downloaded mods, see where each comes from, and quieten the conflicts list
- Open your downloads folder from Settings
- Remember mod lists between visits, and flag mods you must fetch yourself
- Work out where each mod is downloaded from

### Bug Fixes

- **scraper:** Thread slug through DeadlyStream download URLs
- **ci:** Always cut the first release on a tagless repo
- **ci:** Use git-cliff --tag instead of --bump for the changelog
- **ci:** Harden release version handling against shell injection
- **changelog:** Render one bullet per line in cliff.toml template
- Image proxy, reliable external links, custom patcher, scraper names
- **ui:** Clickable build mods, screenshot lightbox, links, patcher, sidebar
- **ui:** Render inline bold in What's New; refresh screenshots
- **scraper:** Keep only the real screenshot gallery
- **security:** Avoid building a command string from a path in reveal_path
- Stop installs failing when antivirus briefly locks a file
- Keep the conflicts list from vanishing after you resolve one
- Make "Open download folder" actually open a folder
- Keep the conflicts badge in sync and make conflicts easier to understand
- App build error after adding library change detection
- Build error caused by TypeScript narrowing in library event handler
- Show friendly install method names in the mod library
- Remove encoding error in mod manager that blocked app startup
- Stop conflicts count from growing and remove duplicate mod names
- Add disable buttons to file-conflict cards in the Conflicts tab
- Stop the installer showing Finished with 0 mods done when something went wrong mid-run
- Stop the installer crashing when a mod includes a loose texture file
- Prevent path traversal in build-guide file deletion
- Stream HoloPatcher logs live and stop it immediately when you cancel
- Extract archives with very long paths and fix the pywinauto fallback crash
- Hide no-action conflicts, skip installed mods on Select All, and cache mod details to disk
- Mod download and compatibility issues
- Stop double installs, wrong-language patches, and reinstall crashes
- UI automation issues
- Install mods buried inside long or nested folders
- Clear duplicate textures that can crash the game
- Stop a mod's patch installing before the mod itself
- Stop the conflicts list crying wolf, and let you clear it in bulk
- Stop flagging a mod's own add-on as incompatible with it
- Show what each mod changes instead of an unexplained conflict warning
- Make bulk uninstall actually run, and show it working
- Show every mod in a build, not just the ones from DeadlyStream
- Stop a damaged settings file from breaking the app for good
- Keep a settings reset from picking up leftovers
- Build the mod patcher from source so releases stop failing
- Get pull request build checks actually running
- Repair mod downloads and make the app easier to navigate

### Refactor

- Move dev scripts to scripts/ and remove the legacy Tkinter UI

### Documentation

- Add GitHub Pages usage site with screenshots
- Show the app in action with fresh screenshots and demo clips
- Explain that the mod patcher is now built, not downloaded
- Keep assistant session links out of commit messages
- Keep assistant session links out of commit messages

### Build & CI

- Run the offline test suite before building
- Keep the app's dependencies up to date automatically
- Tidy the Releases page each week, keeping the 5 newest downloads
- Run the full offline test suite on every build

### Testing

- E2e download/install suite + fixes it surfaced
- Cover build-guide instruction parsing and selective install
- Add coverage for download filtering and folder exclusion parsing
- Add a test that installs every mod in a build guide
- Fix the long path check failing on machines that allow long paths

### Miscellaneous

- Update Cargo.lock after dropping tauri-plugin-shell
- Add build-guide audit and live-verification tooling
- Update the app's libraries and tools to their latest versions
- Merge dependency updates (23 Dependabot PRs)
- Update fastapi requirement from >=0.138.0 to >=0.138.1
- Update requests requirement from >=2.31.0 to >=2.34.2
- Bump actions/setup-python from 5 to 6
- Bump actions/upload-artifact from 4 to 7
- Bump softprops/action-gh-release from 2 to 3
- Bump the npm-minor-and-patch group across 1 directory with 7 updates
- Build guide accuracy, conflict clarity, and mod management
- Bump actions/setup-node from 6 to 7
- Bump actions/setup-python from 6 to 7
- Bump taiki-e/install-action from 2 to 2.85.5
- Bump the cargo-minor-and-patch group across 1 directory with 4 updates
- Bump the npm-minor-and-patch group across 1 directory with 11 updates
- Update pillow requirement from >=12.2.0 to >=12.3.0
- Update fastapi requirement from >=0.138.1 to >=0.141.1
- Update uvicorn requirement from >=0.49.0 to >=0.52.1
- Update cryptography requirement from >=49.0.0 to >=50.0.0
- Update rarfile requirement from >=4.2 to >=4.5
- Clear a security warning and a build warning after the dependency updates
- Bump the npm-minor-and-patch group in /frontend with 3 updates
- Update uvicorn requirement from >=0.52.1 to >=0.52.3
- Bump taiki-e/install-action from 2.85.5 to 2.85.13
- Fix pull request build checks failing to start
- Bump taiki-e/install-action from 2.85.13 to 2.86.5 (#61)
- Update lxml requirement from >=6.1.1 to >=6.1.2 (#62)
- Update uvicorn requirement from >=0.52.3 to >=0.52.4 (#60)
- Bump the npm-minor-and-patch group in /frontend with 3 updates (#63)
- Bump typescript from 6.0.3 to 7.0.2 in /frontend (#57)
- Bump taiki-e/install-action from 2.86.5 to 2.87.0 (#64)
- Bump the npm-minor-and-patch group in /frontend with 3 updates (#65)
- Update cryptography requirement from >=50.0.0 to >=50.0.1 (#66)
- Bump taiki-e/install-action from 2.87.0 to 2.87.5 (#70)
- Bump tauri-plugin-dialog (#67)
- Update lxml requirement from >=6.1.2 to >=6.1.3 (#68)
- Bump the npm-minor-and-patch group in /frontend with 5 updates (#69)
- Bump taiki-e/install-action from 2.87.5 to 2.87.11 (#71)
- Bump the npm-minor-and-patch group in /frontend with 6 updates (#72)
- Update uvicorn requirement from >=0.52.4 to >=0.53.0
- Bump taiki-e/install-action from 2.87.11 to 2.87.15
- Bump the npm-minor-and-patch group in /frontend with 2 updates
- Add GPL-3.0 license
- Bump the npm-minor-and-patch group in /frontend with 3 updates
- Bump taiki-e/install-action from 2.87.15 to 2.87.20
- Bump tauri
- Bump taiki-e/install-action from 2.87.20 to 2.87.22
- Update cryptography requirement from >=50.0.1 to >=50.0.2
- Update fastapi requirement from >=0.141.1 to >=0.142.2
- Update uvicorn requirement from >=0.53.0 to >=0.54.0
- Bump the cargo-minor-and-patch group
- Bump the npm-minor-and-patch group across 1 directory with 6 updates
- Update the Tauri app framework packages together so builds stop breaking

