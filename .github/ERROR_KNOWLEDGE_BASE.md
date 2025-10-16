# 📚 FFmpeg Android ARM32 - Error Knowledge Base

> **Cập nhật:** Tự động bởi AI (Gemini 2.0 Flash)
> **Tổng số lỗi:** 3

---

## 📋 Quick Reference

| ID | Tên lỗi | Thư viện | Workflow | Ngày |
| ERROR-001 | Không có lỗi build nào được ghi nhận trong log | unknown | Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) | 2025-10-16 |
| ERROR-001 | Build process stalled or extremely slow | libass | Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) | 2025-10-16 |
| ERROR-999 | Gemini API failed - Using fallback | unknown | Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) | 2025-10-16 |
|----|---------|----------|----------|------|

---

## 🔴 Chi tiết lỗi

### 🔴 ERROR-999: Gemini API failed - Using fallback

**📅 Ngày:** 2025-10-16

**📦 Workflow:** Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) [Run #10](https://github.com/share-18001080/113/actions/runs/18555283263)

**🎯 Thư viện:** `unknown`

**🤖 Độ tin cậy:** 30%

**⚠️ Triệu chứng:**
```
Unknown error
```

**🔍 Nguyên nhân:**
Unknown error

**🛠️ Fix:**
Cần phân tích thủ công - Gemini API không khả dụng

**📝 Loại:** `UNKNOWN`

---

### 🔴 ERROR-001: Build process stalled or extremely slow

**📅 Ngày:** 2025-10-16

**📦 Workflow:** Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) [#12](https://github.com/share-18001080/113/actions/runs/18555644340)

**🎯 Thư viện:** `libass`

**🤖 Độ tin cậy:** 90%

**⚠️ Triệu chứng:** Build process taking excessively long, Progress bar stuck at a low percentage, Continuous network activity without significant progress

**🔍 Nguyên nhân:** The log shows continuous data transfer, but the progress is very slow (stuck at 29-33%). This could be due to network issues, resource constraints (CPU, memory), or a dependency download failure that is causing repeated retries.

**🛠️ Fix:** 1. Check network connectivity and speed. 2. Increase allocated resources (CPU, memory) for the build process. 3. Verify that all dependencies required by libass are available and accessible. 4. Retry the build with increased verbosity to identify the specific step causing the slowdown.

**📝 Loại:** `PERFORMANCE`

---


### 🔴 ERROR-001: Không có lỗi build nào được ghi nhận trong log

**📅 Ngày:** 2025-10-16

**📦 Workflow:** Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) [#13](https://github.com/share-18001080/113/actions/runs/18556579485)

**🎯 Thư viện:** `unknown`

**🤖 Độ tin cậy:** 100%

**⚠️ Triệu chứng:** 

**🔍 Nguyên nhân:** Không có lỗi

**🛠️ Fix:** Không cần fix

**📝 Loại:** `NONE`

---

