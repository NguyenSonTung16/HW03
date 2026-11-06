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
- [ ] Recording tool is ready. Screen recording is optional; audio is recorded only with the participant’s explicit consent.
- [ ] Print or open one blank observation log and one post-task questionnaire for this participant.
- [ ] Prepare a private contact/eligibility list outside this repository; use participant codes in the submitted materials.

## 3. Moderator opening and consent

Read this in a neutral tone and adapt it only after student review:

> Thank you for taking part. We are evaluating the EShop interface, not you. There are no right or wrong actions. Please use the store as you normally would and say what you are thinking when comfortable. You may stop at any time. We will not place a real order or use real payment or personal details. I would like to record the screen [and audio, if requested] so I can review what happened. Recording is optional; may I record the screen [and audio] for this session?

- Record the participant’s decision and the specific scope of consent before recording.
- If the participant declines recording, continue with written notes only if they still agree to participate.
- Do not collect more personal data than the assignment requires. Store identity/contact verification privately; use a participant code in this repository and report.

## 4. Participant-facing task

> Imagine you are considering buying a product from this store. Find a product you would consider buying, learn enough to decide, and check what you would pay at checkout. You have the discount code `SAVE10` and want to see whether it applies. Stop at the checkout review step before placing an order. Please say what you are thinking as you go. You do not need to enter real personal or payment information.

Do not tell the participant which control to click or where a feature is located. If they ask for help, first say: “What would you expect to do next?” If they remain completely blocked, give only the minimum neutral prompt, record it, and mark the point as moderator-assisted.

## 5. Session procedure

1. Assign a participant code (for example `P01`); verify privately that the person meets the assignment’s eligibility requirement and is outside the class.
2. Explain the study, voluntary participation, stopping at any time, and the no-real-order boundary. Obtain consent before any recording.
3. Start the observation log and note environment details. Do not coach or explain the interface.
4. Read the task once. Ask the participant to think aloud; do not narrate their actions for them.
5. Observe neutrally. Record timestamps, actions, hesitations, errors, quotes, task outcome, and any moderator prompt. Intervene only if they are completely stuck or safety/privacy could be affected.
6. End at checkout review; do not submit a real order. Stop recording and confirm the participant is comfortable with the session ending.
7. Have the participant complete the chosen SUS questionnaire immediately after the task and before debriefing. Then ask the open questions below.
8. Thank the participant. Save the anonymized notes and consent/recording status securely. Do not publish raw contact details or recordings in GitHub.

## 6. Post-task open questions

Ask the same questions in the same order, without suggesting an answer:

1. Which part of the task, if any, was least clear?
2. When something did not behave as you expected, what did you think was happening?
3. How did the pace of the task feel? What affected it?
4. At the checkout review step, how confident were you that the displayed order and total were correct? What led you to that view?
5. If you could change one thing in the experience, what would you change first?

Record the participant’s words as accurately as possible and distinguish direct quotes from the moderator’s summary.

## 7. SUS questionnaire — Vietnamese working translation

Use the same wording and language for all seven formal sessions. This Vietnamese wording is a working translation of the original SUS items, not a verified or published Vietnamese version. The student must review the translation and test comprehension in the pilot. If the scale wording is changed after the pilot, document the change and use one consistent final version for all seven sessions.

For each statement select one value: **1 Hoàn toàn không đồng ý · 2 Không đồng ý · 3 Trung lập · 4 Đồng ý · 5 Hoàn toàn đồng ý**.

1. Tôi nghĩ rằng tôi sẽ muốn sử dụng hệ thống này thường xuyên. `1  2  3  4  5`
2. Tôi thấy hệ thống này phức tạp một cách không cần thiết. `1  2  3  4  5`
3. Tôi nghĩ hệ thống này dễ sử dụng. `1  2  3  4  5`
4. Tôi nghĩ tôi cần sự hỗ trợ của người có chuyên môn kỹ thuật để sử dụng được hệ thống này. `1  2  3  4  5`
5. Tôi nhận thấy các chức năng trong hệ thống được tích hợp tốt với nhau. `1  2  3  4  5`
6. Tôi nghĩ hệ thống này có quá nhiều điểm không nhất quán. `1  2  3  4  5`
7. Tôi nghĩ hầu hết mọi người sẽ học cách dùng hệ thống này rất nhanh. `1  2  3  4  5`
8. Tôi thấy hệ thống này rất bất tiện khi sử dụng. `1  2  3  4  5`
9. Tôi cảm thấy tự tin khi sử dụng hệ thống. `1  2  3  4  5`
10. Tôi cần học nhiều điều trước khi có thể bắt đầu sử dụng hệ thống này. `1  2  3  4  5`

**Scoring:** items 1, 3, 5, 7, 9 contribute response − 1; items 2, 4, 6, 8, 10 contribute 5 − response. Sum the ten contributions and multiply by 2.5 for a 0–100 SUS score. Calculate only after collecting real responses; never fill a response on a participant’s behalf. Report the seven individual scores and a clearly described summary, without presenting the score as a percentage.

## 8. Pilot review checklist

- [ ] Participant understands the task without instructions about individual controls.
- [ ] The chosen flow is possible in the isolated SUT and stops before an order is placed.
- [ ] The discount code/test data are ready and do not require real personal/payment details.
- [ ] Consent wording and recording choice are clear; refusal can be handled without pressure.
- [ ] Observation log captures actions, time, hesitation, error, quote, result, and moderator intervention.
- [ ] Participant understands every SUS item and the response scale; note confusing wording without changing it mid-session.
- [ ] Record actual pilot duration and all changes made to the script, form, environment, and questionnaire.
- [ ] Finalize the materials before beginning the seven formal sessions.

## 9. Human-only actions still outstanding

- Recruit and verify the pilot participant and seven eligible formal participants.
- Explain the study and obtain each participant’s actual consent; request recording consent separately.
- Conduct the pilot and seven sessions, observe behavior, administer the questionnaire, and record genuine answers.
- Keep contact information and any recordings private; anonymize the submitted notes.

## Sources

- Assignment plan: `planning/HW03_Ke_hoach_va_checklist.md`, Phase C and participant preparation.
- Brooke, J. (1996), “SUS: A quick and dirty usability scale.” [Source text](https://hci-studies.org/methods-and-measures/downloads/SUS_Brooke1996.pdf). The source describes the ten statements, immediate post-task administration, and scoring formula.
