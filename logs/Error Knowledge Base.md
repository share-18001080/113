# FFmpeg Android ARM32 - Error Knowledge Base

> **Purpose:** Track all build errors for FFmpeg Android ARM32
> **AI:** Gemini 2.0 Flash with detail log analysis
> **Storage:** All logs in `/logs/` folder (Perplexity-optimized)
> **Total Errors:** 9

## Quick Reference

| ID | Error | Library | Version | Summary | Date |
| ERROR-001 | Freetype library not found despite HB_HAVE_FREETYPE being set. | libass | ver14 | [`Build FFmpeg Android ARM32 Full Features LibSOXR Fixed Freetype2 Dependencies - ver14 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibSOXR Fixed Freetype2 Dependencies - ver14 run1 20251017.md) | 2025-10-17 |
| ERROR-001 | freetype2 dependency not found | libass | ver13 | [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver13 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver13 run1 20251017.md) | 2025-10-17 |
| ERROR-001 | Invalid value for Fontconfig support option in Meson build. | libass | ver12 | [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver12 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver12 run1 20251017.md) | 2025-10-17 |
| ERROR-LASS-001 | Meson build failed: Value disabled is not boolean | libass | ver11 | [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver11 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver11 run1 20251017.md) | 2025-10-17 |
| ERROR-001 | Missing system font provider for libass compilation | libass | ver10 | [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver10 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver10 run1 20251017.md) | 2025-10-17 |
| ERROR-001 | Harfbuzz dependency not found for libass | libass | ver9 | [`Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run1 20251017.md) | 2025-10-17 |
| ERROR-001 | Harfbuzz dependency not found for libass build. | libass | ver9 | [`Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run24 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run24 20251017.md) | 2025-10-17 |
| ERROR-001 | Harfbuzz dependency not found during libass build | libass | ver9 | [`Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run21 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run21 20251017.md) | 2025-10-17 |
| ERROR-001 | Dependency harfbuzz not found for libass | libass | ver9 | [`B u i l d F F m p e g A n d r o i d A R M 3 2 F u l l F e a t u r e s L i b A S S C O M P L E T E L Y F I X E D - v e r 9 - f i x e d run19 20251017.md`](Error Summaries/B u i l d F F m p e g A n d r o i d A R M 3 2 F u l l F e a t u r e s L i b A S S C O M P L E T E L Y F I X E D - v e r 9 - f i x e d run19 20251017.md) | 2025-10-17 |
|----|-------|---------|---------|---------|------|

## Error Details


### 🔴 ERROR-001: Dependency harfbuzz not found for libass

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #19](https://github.com/share-18001080/113/actions/runs/18588660670)
**🎯 Library:** `libass`
**🏷️ Version:** `ver9`
**🤖 AI Confidence:** 90%
**📄 Full Summary:** [`B u i l d F F m p e g A n d r o i d A R M 3 2 F u l l F e a t u r e s L i b A S S C O M P L E T E L Y F I X E D - v e r 9 - f i x e d run19 20251017.md`](Error Summaries/B u i l d F F m p e g A n d r o i d A R M 3 2 F u l l F e a t u r e s L i b A S S C O M P L E T E L Y F I X E D - v e r 9 - f i x e d run19 20251017.md)
**📋 Detail Log:** [`meson-log ver9 run19.txt`](Detail Logs/meson-log ver9 run19.txt)
**⚠️ Symptoms:** Build fails, Missing harfbuzz dependency
**🔍 Root Cause:** The libass build process requires the harfbuzz library, but it could not be found using pkg-config.
**🛠️ Fix Suggestion:** Install the harfbuzz library and its development headers. Ensure pkg-config can find it by setting PKG_CONFIG_PATH or similar. If harfbuzz is installed in a non-standard location, provide the correct path to pkg-config. Alternatively, disable harfbuzz support in libass if it's not strictly required.
**📝 Type:** `DEPENDENCY`

---


### 🔴 ERROR-001: Harfbuzz dependency not found during libass build

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #21](https://github.com/share-18001080/113/actions/runs/18589222542)
**🎯 Library:** `libass`
**🏷️ Version:** `ver9`
**🤖 AI Confidence:** 90%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run21 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run21 20251017.md)
**📋 Detail Log:** [`meson-log ver9 run21.txt`](Detail Logs/meson-log ver9 run21.txt)
**⚠️ Symptoms:** Build failure, Missing harfbuzz dependency
**🔍 Root Cause:** The Meson build system for libass could not locate the harfbuzz dependency using pkg-config. This indicates that harfbuzz is either not installed, not configured correctly, or pkg-config is not finding it in the expected location.
**🛠️ Fix Suggestion:** Install harfbuzz and ensure it's discoverable by pkg-config. Verify that PKG_CONFIG_PATH includes the directory containing harfbuzz's .pc file. If harfbuzz is installed in a non-standard location, explicitly set PKG_CONFIG_PATH before running the build. Alternatively, provide the path to harfbuzz using meson configure options.
**📝 Type:** `DEPENDENCY`

---


### 🔴 ERROR-001: Harfbuzz dependency not found for libass build.

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #24](https://github.com/share-18001080/113/actions/runs/18589680069)
**🎯 Library:** `libass`
**🏷️ Version:** `ver9`
**🤖 AI Confidence:** 95%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run24 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run24 20251017.md)
**📋 Detail Log:** [`meson-log ver9 run24.txt`](Detail Logs/meson-log ver9 run24.txt)
**⚠️ Symptoms:** Build fails during libass configuration., Error message indicates missing harfbuzz dependency., Meson log shows failure to find harfbuzz via pkg-config.
**🔍 Root Cause:** The build system (Meson) could not locate the harfbuzz library, which is a dependency of libass. The system tried pkg-config but failed.
**🛠️ Fix Suggestion:** Install the harfbuzz library and its development headers. Ensure pkg-config is correctly configured to find harfbuzz. If harfbuzz is installed in a non-standard location, set the PKG_CONFIG_PATH environment variable to include the directory containing harfbuzz's .pc file. Alternatively, provide the path to harfbuzz using Meson's dependency options.
**📝 Type:** `DEPENDENCY`

---


### 🔴 ERROR-001: Harfbuzz dependency not found for libass

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #1](https://github.com/share-18001080/113/actions/runs/18590219901)
**🎯 Library:** `libass`
**🏷️ Version:** `ver9`
**🤖 AI Confidence:** 95%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS COMPLETELY FIXED - ver9-fixed run1 20251017.md)
**📋 Detail Log:** [`meson-log ver9 run1.txt`](Detail Logs/meson-log ver9 run1.txt)
**⚠️ Symptoms:** Build fails during libass configuration, Meson reports 'Dependency "harfbuzz" not found'
**🔍 Root Cause:** The build system (Meson) could not locate the harfbuzz library using pkg-config. This indicates that harfbuzz is either not installed, not configured correctly, or pkg-config is not finding it in the expected location.
**🛠️ Fix Suggestion:** Install harfbuzz and ensure pkg-config can find it. Verify that the PKG_CONFIG_PATH environment variable includes the directory containing harfbuzz's .pc file. If harfbuzz is installed in a non-standard location, explicitly set PKG_CONFIG_PATH before running the build. Alternatively, provide harfbuzz's location directly to Meson if possible.
**📝 Type:** `DEPENDENCY`

---


### 🔴 ERROR-001: Missing system font provider for libass compilation

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #1](https://github.com/share-18001080/113/actions/runs/18591621474)
**🎯 Library:** `libass`
**🏷️ Version:** `ver10`
**🤖 AI Confidence:** 90%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver10 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver10 run1 20251017.md)
**📋 Detail Log:** [`meson-log ver10 run1.txt`](Detail Logs/meson-log ver10 run1.txt)
**⚠️ Symptoms:** Compilation fails, Missing font provider
**🔍 Root Cause:** Libass requires a system font provider (DirectWrite, Core Text, or Fontconfig) to compile. None were found, and `-Drequire-system-font-provider=false` was not set.
**🛠️ Fix Suggestion:** Install a system font provider like Fontconfig, DirectWrite (Windows), or Core Text (macOS). Alternatively, if you don't need a system font provider, set the Meson option `-Drequire-system-font-provider=false` during configuration. Ensure the necessary dependencies for the chosen font provider are also installed.
**📝 Type:** `DEPENDENCY`

---


### 🔴 ERROR-LASS-001: Meson build failed: Value disabled is not boolean

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #1](https://github.com/share-18001080/113/actions/runs/18592283653)
**🎯 Library:** `libass`
**🏷️ Version:** `ver11`
**🤖 AI Confidence:** 95%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver11 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver11 run1 20251017.md)
**📋 Detail Log:** [`meson-log ver11 run1.txt`](Detail Logs/meson-log ver11 run1.txt)
**⚠️ Symptoms:** Build failure, Meson configuration error, Non-boolean value for boolean option
**🔍 Root Cause:** The Meson build system expects a boolean value (true or false) for a configuration option, but it received 'disabled' instead. This likely indicates an incorrect configuration setting passed to Meson during the libass build process.
**🛠️ Fix Suggestion:** Check the Meson configuration files (meson.build) and the arguments passed to Meson during the build process. Ensure that all boolean options are set to either 'true' or 'false'. Review the build scripts and environment variables to identify where the incorrect 'disabled' value is being set and correct it to a valid boolean value. Examine the meson-log.txt file for more detailed information about the configuration error.
**📝 Type:** `CONFIGURE`

---


### 🔴 ERROR-001: Invalid value for Fontconfig support option in Meson build.

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #1](https://github.com/share-18001080/113/actions/runs/18593007496)
**🎯 Library:** `libass`
**🏷️ Version:** `ver12`
**🤖 AI Confidence:** 90%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver12 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver12 run1 20251017.md)
**📋 Detail Log:** [`meson-log ver12 run1.txt`](Detail Logs/meson-log ver12 run1.txt)
**⚠️ Symptoms:** Build fails during the configuration stage., Meson build system reports an error related to Fontconfig support.
**🔍 Root Cause:** The Meson build system received an invalid string value ('false') for the 'Fontconfig support' option. It expects 'enabled', 'disabled', or 'auto'.
**🛠️ Fix Suggestion:** Modify the build configuration to provide a valid value ('enabled', 'disabled', or 'auto') for the 'Fontconfig support' option. Check the build scripts or configuration files for the incorrect value and replace it with a valid one. Ensure the build system is correctly passing the desired option value to Meson.
**📝 Type:** `CONFIGURE`

---


### 🔴 ERROR-001: freetype2 dependency not found

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #1](https://github.com/share-18001080/113/actions/runs/18593808259)
**🎯 Library:** `libass`
**🏷️ Version:** `ver13`
**🤖 AI Confidence:** 95%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver13 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibASS Harfbuzz COMPLETELY FIXED - ver13 run1 20251017.md)
**📋 Detail Log:** [`meson-log ver13 run1.txt`](Detail Logs/meson-log ver13 run1.txt)
**⚠️ Symptoms:** Build fails due to missing freetype2 dependency.
**🔍 Root Cause:** The build process requires the freetype2 library, but it could not be found by pkg-config or CMake.
**🛠️ Fix Suggestion:** Install the freetype2 development package using your system's package manager. For Debian/Ubuntu, use 'sudo apt-get install libfreetype6-dev'. Ensure pkg-config can find the library by setting PKG_CONFIG_PATH if necessary. Verify freetype2 is correctly installed and configured.
**📝 Type:** `DEPENDENCY`

---


### 🔴 ERROR-001: Freetype library not found despite HB_HAVE_FREETYPE being set.

**📅 Date:** 2025-10-17
**🔗 GitHub:** [Run #1](https://github.com/share-18001080/113/actions/runs/18603721483)
**🎯 Library:** `libass`
**🏷️ Version:** `ver14`
**🤖 AI Confidence:** 90%
**📄 Full Summary:** [`Build FFmpeg Android ARM32 Full Features LibSOXR Fixed Freetype2 Dependencies - ver14 run1 20251017.md`](Error Summaries/Build FFmpeg Android ARM32 Full Features LibSOXR Fixed Freetype2 Dependencies - ver14 run1 20251017.md)
**⚠️ Symptoms:** Build fails during CMake configuration., Freetype not found error message.
**🔍 Root Cause:** The build system expects Freetype to be available because HB_HAVE_FREETYPE is enabled, but the Freetype library and include directories cannot be located by CMake.
**🛠️ Fix Suggestion:** Ensure Freetype2 is installed and the CMAKE_PREFIX_PATH variable points to the Freetype2 installation directory. Alternatively, disable HB_HAVE_FREETYPE if Freetype is not intended to be used. Verify that FREETYPE_LIBRARY and FREETYPE_INCLUDE_DIRS are correctly set in CMake.
**📝 Type:** `CONFIGURE`

---

