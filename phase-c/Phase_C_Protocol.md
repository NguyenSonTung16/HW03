# Phase C — Usability Evaluation Protocol (Draft)

**Status:** preparation draft; not a record of participant activity. The student must review and finalize this protocol, recruit eligible people, obtain consent, moderate every session, and record only real observations and responses.

## 1. Study scope

- **SUT:** isolated EShop SUT. Record the exact build/commit, URL, browser, operating system, viewport, and test account used for each session.
- **One end-to-end flow:** find a product, inspect it, place it in the cart, try the selected discount code, review the total, and reach the checkout review step.
- **Research goal:** learn whether a target user can find a suitable product, understand the product and cart information, apply a discount, and determine whether the order is ready for checkout without moderator guidance.
- **Participant group:** seven real people outside the HW03 class, one participant per formal session. Prefer people without software/QA experience where practical; this is a preference, not an eligibility requirement. Keep verifiable contact details private and do not commit them to Git.
- **Pilot:** one real person before the seven formal sessions. Keep the pilot separate from the seven to avoid ambiguity in the assignment.

## 2. Materials and setup

- [ ] Student has reviewed this AI-generated draft and confirmed the exact task, questionnaire language, and recording plan.
- [ ] EShop isolated environment is running and contains no real orders or personal data.
- [ ] Browser starts from a clean session with an empty cart and the intended account state.
- [ ] Prepare a test-only product choice, discount code `SAVE10`, and clearly fictitious checkout values if the task needs them. Never request a participant’s real address, phone, payment, or account password.
- [ ] Recording tool is ready. The assignment asks to record the screen; ask before recording. Audio is recorded only with explicit consent. If screen recording is declined, take structured notes and mark the missing recording; seek a consenting participant for a formal session with complete evidence.
- [ ] Print or open one blank observation log and one post-task questionnaire for this participant.
- [ ] Prepare a private contact/eligibility list outside this repository; use participant codes in the submitted materials.

## 3. Bộ công cụ dùng cho phiên

- [Hướng dẫn sử dụng](Huong_dan_su_dung_bo_cong_cu.md): thứ tự pilot, bảy phiên và tổng hợp.
- [Phiếu nhiệm vụ và SUS cho người tham gia](Kich_ban_nguoi_tham_gia.md): **bản câu chữ cần dùng thống nhất** sau khi sinh viên rà soát và pilot.
- [Phiếu điều phối và ghi nhận](Phieu_dieu_phoi_va_ghi_nhan.md): lời giới thiệu, xin đồng ý, quan sát và hỏi sau nhiệm vụ.
- [Bảng sự kiện trống](Observation_Log_TEMPLATE.csv) và [bảng theo dõi bằng mã trống](Participant_Tracker_TEMPLATE.csv).

Các mẫu này chưa chứa người tham gia hoặc kết quả thật. Việc tuyển người, xin đồng ý, điều phối, ghi nhận và chọn bản SUS cuối phải do sinh viên thực hiện. Bản tiếng Việt của SUS là bản dịch làm việc từ [thang gốc của Brooke (1996)](https://hci-studies.org/methods-and-measures/downloads/SUS_Brooke1996.pdf); không ghi là bản dịch đã được chuẩn hóa.

## 4. Pilot review checklist

- [ ] Participant understands the task without instructions about individual controls.
- [ ] The chosen flow is possible in the isolated SUT and stops before an order is placed.
- [ ] The discount code/test data are ready and do not require real personal/payment details.
- [ ] Consent wording and recording choice are clear; refusal can be handled without pressure.
- [ ] Observation log captures actions, time, hesitation, error, quote, result, and moderator intervention.
- [ ] Participant understands every SUS item and the response scale; note confusing wording without changing it mid-session.
- [ ] Record actual pilot duration and all changes made to the script, form, environment, and questionnaire.
- [ ] Finalize the materials before beginning the seven formal sessions.

## 5. Human-only actions still outstanding

- Recruit and verify the pilot participant and seven eligible formal participants.
- Explain the study and obtain each participant’s actual consent; request recording consent separately.
- Conduct the pilot and seven sessions, observe behavior, administer the questionnaire, and record genuine answers.
- Keep contact information and any recordings private; anonymize the submitted notes.

## Sources

- Assignment plan: `planning/HW03_Ke_hoach_va_checklist.md`, Phase C and participant preparation.
- Brooke, J. (1996), “SUS: A quick and dirty usability scale.” [Source text](https://hci-studies.org/methods-and-measures/downloads/SUS_Brooke1996.pdf). The source describes the ten statements, immediate post-task administration, and scoring formula.
