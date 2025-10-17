# FFmpeg Android ARM32 - Error Knowledge Base

> **Purpose:** Track all build errors for FFmpeg Android ARM32
> **AI:** Gemini 2.0 Flash with detail log analysis
> **Storage:** All logs in `/logs/` folder (Perplexity-optimized)
> **Total Errors:** 3

## Quick Reference

| ID | Error | Library | Version | Summary | Date |
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

