# FFmpeg Android ARM32 - Error Knowledge Base

> **Purpose:** Track all build errors for FFmpeg Android ARM32
> **AI:** Gemini 2.0 Flash with detail log analysis
> **Storage:** All logs in `/logs/` folder (Perplexity-optimized)
> **Total Errors:** 1

## Quick Reference

| ID | Error | Library | Version | Summary | Date |
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

