# 📚 FFmpeg Android ARM32 - Error Knowledge Base

> **AI:** Gemini with detail log files  
> **Total:** 

## 📋 Quick Reference

| ID | Error | Library | Ver | Summary | Date |
| ERROR-001 | Meson build failed due to unknown options | libass | ver8 | [`Build_FFmpeg_Android_ARM32__Full_Features___LibASS_Added_-_ver8__run45_20251016-151056.md`](.github/error-summaries/Build_FFmpeg_Android_ARM32__Full_Features___LibASS_Added_-_ver8__run45_20251016-151056.md) | 2025-10-16 |
|----|-------|---------|-----|---------|------|

## 🔴 Details


### 🔴 ERROR-001: Meson build failed due to unknown options

**📅** 2025-10-16 | **🔗** [Run #45](https://github.com/share-18001080/113/actions/runs/18565709307)  
**🎯** `libass` | **🏷️** `ver8` | **🤖** 90%

**📄 Summary:** [`Build_FFmpeg_Android_ARM32__Full_Features___LibASS_Added_-_ver8__run45_20251016-151056.md`](.github/error-summaries/Build_FFmpeg_Android_ARM32__Full_Features___LibASS_Added_-_ver8__run45_20251016-151056.md)  
**📋 Detail Log:** `/home/runner/work/113/113/external/libass/build/meson-logs/meson-log.txt`

**⚠️** Build process exits with code 1, Meson reports 'Unknown options: "harfbuzz, libtool"', LibASS build fails  
**🔍** The Meson build system for libass does not recognize the 'harfbuzz' and 'libtool' options. This likely indicates a configuration error in the build script or an outdated Meson version that doesn't support these options, or the options are named differently.  
**🛠️** Update Meson to the latest version. Review the libass meson.build file for correct option names and usage. Ensure harfbuzz and libtool dependencies are correctly installed and configured for cross-compilation. Check if these options are deprecated or renamed in newer versions of libass.

---

