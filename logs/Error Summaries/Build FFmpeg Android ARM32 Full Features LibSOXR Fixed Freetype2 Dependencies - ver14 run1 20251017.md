# FFmpeg Build Error Summary

## Workflow Info

- **Name:** Build FFmpeg Android ARM32 (Full Features + LibSOXR + Fixed Freetype2 Dependencies - ver14)
- **Run:** #1
- **Version:** ver14
- **Date:** 2025-10-17 20:15:55
- **Status:** Failed
- **GitHub:** https://github.com/share-18001080/113/actions/runs/18603721483

## AI Analysis (Gemini 2.0 Flash)

```json
{
"error_id": "ERROR-001",
"error_name": "Freetype library not found despite HB_HAVE_FREETYPE being set.",
"root_cause": "The build system expects Freetype to be available because HB_HAVE_FREETYPE is enabled, but the Freetype library and include directories cannot be located by CMake.",
"affected_library": "libass",
"error_type": "CONFIGURE",
"symptoms": [
"Build fails during CMake configuration.",
"Freetype not found error message."
],
"fix_suggestion": "Ensure Freetype2 is installed and the CMAKE_PREFIX_PATH variable points to the Freetype2 installation directory. Alternatively, disable HB_HAVE_FREETYPE if Freetype is not intended to be used. Verify that FREETYPE_LIBRARY and FREETYPE_INCLUDE_DIRS are correctly set in CMake.",
"confidence": 90
}
```

### Error Details

**Error ID:** ERROR-001
**Error Name:** Freetype library not found despite HB_HAVE_FREETYPE being set.
**Affected Library:** libass
**Error Type:** CONFIGURE
**AI Confidence:** 90%

**Symptoms:**

- Build fails during CMake configuration.
- Freetype not found error message.

**Root Cause:**

The build system expects Freetype to be available because HB_HAVE_FREETYPE is enabled, but the Freetype library and include directories cannot be located by CMake.

**Fix Suggestion:**

Ensure Freetype2 is installed and the CMAKE_PREFIX_PATH variable points to the Freetype2 installation directory. Alternatively, disable HB_HAVE_FREETYPE if Freetype is not intended to be used. Verify that FREETYPE_LIBRARY and FREETYPE_INCLUDE_DIRS are correctly set in CMake.

## Error Context (20 lines before exit code)

```
2025-10-17T20:15:34.5003264Z   CMake.
2025-10-17T20:15:34.5003424Z 
2025-10-17T20:15:34.5003733Z   Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
2025-10-17T20:15:34.5004742Z   to tell CMake that the project requires at least <min> but has been updated
2025-10-17T20:15:34.5005395Z   to work with policies introduced by <max> or earlier.
2025-10-17T20:15:34.5005883Z Call Stack (most recent call first):
2025-10-17T20:15:34.5006558Z   /opt/hostedtoolcache/ndk/r25c/x64/build/cmake/android.toolchain.cmake:54 (include)
2025-10-17T20:15:34.5007634Z   /home/runner/work/113/113/external/harfbuzz/build_android/CMakeFiles/3.31.6/CMakeSystem.cmake:6 (include)
2025-10-17T20:15:34.5009019Z   /home/runner/work/113/113/external/harfbuzz/build_android/CMakeFiles/CMakeScratch/TryCompile-IoWPq1/CMakeLists.txt:4 (project)
2025-10-17T20:15:34.5010028Z 
2025-10-17T20:15:34.5010040Z 
2025-10-17T20:15:34.5643350Z -- Check if compiler accepts -pthread - yes
2025-10-17T20:15:34.5653100Z -- Found Threads: TRUE
2025-10-17T20:15:34.6032505Z -- Could NOT find Freetype (missing: FREETYPE_LIBRARY FREETYPE_INCLUDE_DIRS) 
2025-10-17T20:15:34.6033115Z CMake Error at CMakeLists.txt:235 (message):
2025-10-17T20:15:34.6033518Z   HB_HAVE_FREETYPE was set, but we failed to find it.  Maybe add a
2025-10-17T20:15:34.6033957Z   CMAKE_PREFIX_PATH= to your Freetype2 install prefix
2025-10-17T20:15:34.6034206Z 
2025-10-17T20:15:34.6034212Z 
2025-10-17T20:15:34.6035141Z -- Configuring incomplete, errors occurred!
2025-10-17T20:15:34.6093907Z ##[error]Process completed with exit code 1.
```


---

**For Perplexity:** Read this summary in the `logs/Error Summaries/` folder and suggest detailed fix steps.
