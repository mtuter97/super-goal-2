# SPEC KIT: Super Goal 2 Master Interactive Learning & Certification Platform
> **Project Continuation Specification & Architectural Blueprint**  
> **Course:** Super Goal 2 (Intermediate Second Grade – Term 1)  
> **Authority:** Saudi Ministry of Education Curriculum Standards (McGraw-Hill)  
> **Supervising Instructor:** Teacher Mahmoud Al-Saeed  
> **Version:** 3.0 (Phase 3 Completed: Units 1, 2, 3, 4, 5 & 6 Fully Implemented)  
> **Last Updated:** October 2026 (Phase 1, Phase 2 & Phase 3 Completed)

---

## 1. Executive Summary & Purpose

This document serves as the **Master Specification Kit (Spec Kit)** for the **Super Goal 2** interactive educational platform. Any AI assistant or developer opening a new chat session must read this document first to resume development seamlessly without breaking existing architecture, visual guidelines, or curriculum standards.

The core philosophy of this project is to transform traditional textbook documents into a **self-contained, deeply interactive, culturally enriched, zero-backend, 100% Target Language Immersion platform** for Saudi intermediate students.

---

## 2. Invariants & Non-Negotiable Rules

When extending or maintaining this project in any session, adhere strictly to the following 6 rules:

1. **Zero Arabic in Web Source Files:**  
   `index.html`, `styles.css`, `app.js`, and `data.js` must contain **0 Arabic characters**. All UI text, instructions, definitions, explanations, and certificate texts must be in high-standard, accessible English for students. (Communication with the user in chat remains in friendly, professional Arabic).
2. **Pacing Rule ("وحدتين بوحدتين"):**  
   Development proceeds **strictly two units at a time**.  
   - **Phase 1 (Completed):** Units 1 & 2  
   - **Phase 2 (Completed):** Units 3 & 4  
   - **Phase 3 (Completed):** Units 5 & 6  
   - **Phase 4 (Next Step / الخطوة القادمة):** Units 7 & 8  
   *Do not jump ahead to future units until requested by the user.*
3. **Visual Identity & Color Palette:**  
   - Theme is **Light, Vibrant, and Engaging** (crisp backgrounds: `#f8fafc`, `#ffffff`, `#fff7f4`).
   - Primary Brand Color derived from the Teacher's Official Logo (`assets/images/teacher_logo.jpg`): **Warm Terracotta Coral** (`#e7713f`, `#cf5927`).
   - Saudi Cultural Accent: **Saudi Emerald Green** (`#059669`, `#047857`, `#ecfdf5`).
   - Academic Honor Accent: **Radiant Gold** (`#d97706`, `#f59e0b`).
   - Secondary Tech Accents: **Slate Charcoal** (`#2d3748`) and **Sky Blue** (`#0284c7`).
   - The Teacher Logo must remain prominently visible in the header (with a verified badge), footer, and on the official certificate.
4. **Interactive Student Registration & Certification Gateway:**  
   - Top-level **Student Passport Bar** where students enter their English name and school.
   - Persistent `localStorage` tracking for student identity and gamified XP points.
   - Direct button `📜 Claim Certificate` allowing students to preview, generate, and print their official Certificate of Distinction.
5. **Authentic Saudi Cultural Context in Every Section:**  
   - Real photos from Saudi Arabia: Holy Kaaba, Grand Mosque Expansion, Al-Ula Hegra UNESCO monument, Vision 2030 future skyline, Islamic calligraphy, S.A.Y.H.A. youth hostels across 21 cities, authentic Saudi Kabsa culinary traditions, and the National Museum of Saudi Arabia.
   - High-resolution modal zoom when clicking any photo.
   - Visual clue badges on quiz and examination questions (`🍽️ Restaurant Dining`, `📜 Arabic Calligraphy`, `🏛️ Museum Exhibits`, `🏨 Hotel Encounter`, `🇸🇦 Saudi Geography`).
   - Pedagogical explanations for every question explaining why the correct choice is right and analyzing distractors.
6. **Teacher Signature & Endorsement:**  
   Official certificates of achievement must feature:
   $$\begin{array}{c}
   \textbf{Teacher: Mahmoud Al-Saeed} \\
   \text{English Language Instructor \& Academic Supervisor}
   \end{array}$$

---

## 3. Current Project State (Phase 1, Phase 2 & Phase 3: Units 1 to 6 Completed)

### Key Metrics Summary
| Metric | Current Count | Status |
| :--- | :---: | :---: |
| **Units Implemented** | 6 Units (Units 1, 2, 3, 4, 5 & 6) | ✅ 100% Complete |
| **Total Vocabulary Items** | 252 words & expressions | ✅ With IPA, definitions, examples, audio & Saudi context |
| **Grammar Modules** | 14 modules | ✅ With formulas, comparison tables & 56 diagnostics |
| **Pronunciation Labs** | 6 units | ✅ Intonation, Vowels, Reductions, Stress, Plurals (/s/,/z/,/ɪz/) & Past (-ed /t/,/d/,/ɪd/) |
| **Reading Stories** | 6 full passages | ✅ With 30 comprehension items & 27 gallery photos |
| **Saudi Cultural Showcase** | 10 high-resolution cards | ✅ Kaaba, Mosque expansion, Al-Ula, Vision 2030, Calligraphy, SAYHA, Tech Careers, SAFCSP Drones, Saudi Hospitality, National Museum |
| **High-Resolution Images** | 62 images in `assets/images` | ✅ Extracted from book and cultural archives |
| **Writing Master Tasks** | 6 interactive tasks | ✅ With live word count & keyword evaluator |
| **Discussion Scenarios** | 18 real-life simulations | ✅ With scripted audio dialogue & model responses |
| **Tiered Examinations** | 30 exams (20 Qs each) | ✅ 600 questions with visual clues & comprehensive explanations |
| **Arabic Characters in Web Code** | **0** | ✅ Verified 100% Target Language Immersion |

---

## 4. File Structure & Responsibilities

```text
c:\Users\elsae\Desktop\grade2 primary project\
├── SPEC_KIT.md                     # THIS FILE: Master Specification Kit for new chats
├── index.html                      # Semantic HTML5 layout, Passport bar, 8 tab panes, image modal, certificate modal
├── styles.css                      # Light terracotta & emerald design system, responsive styles, print media
├── app.js                          # Interactive engine (Passport state, Web Audio synthesizer, speech, filters, timer, cert)
├── data.js                         # Centralized JSON database (window.APP_DATA) with Saudi cultural showcase
│
├── assets/
│   └── images/
│       ├── teacher_logo.jpg                # Teacher Mahmoud Al-Saeed's official circular logo
│       ├── super_goal_2_cover.jpg          # Original Super Goal 2 textbook cover
│       ├── holy_kaaba_aerial.jpeg          # Saudi Cultural Showcase: The Holy Kaaba, Makkah
│       ├── holy_mosque_makkah.jpeg         # Saudi Cultural Showcase: Grand Mosque Expansion
│       ├── saudi_alula_heritage.jpg        # Saudi Cultural Showcase: Al-Ula / Hegra Monument
│       ├── u1_reading_future_city.jpeg     # Saudi Cultural Showcase: Riyadh Vision 2030 Skyline
│       ├── saudi_calligraphy_art.jpg       # Saudi Cultural Showcase: Islamic Calligraphy & Art
│       ├── u1_youth_hostel_dorm.jpg        # Unit 1 Reading: shared bunk beds in youth hostel (SAYHA)
│       ├── u1_hostel_social_activities.jpg # Unit 1 Reading: SAYHA youth social activities & sports
│       ├── u1_hostel_historic_building.jpg # Unit 1 Reading: historic castle hostel
│       ├── u1_hostel_kitchen_cooking.jpg   # Unit 1 Reading: communal self-service kitchen
│       ├── u1_town_map_directions.jpg      # Unit 1 FMF: town map for directions
│       ├── u1_reading_discuss_photo.jpeg   # Saudi students in dialogue
│       ├── unit1_unification.jpg           # Historical founding / Unification of Saudi Arabia
│       ├── unit1_vision2030.jpg            # Vision 2030 official emblem
│       ├── u2_film_studio_scene.jpg        # Unit 2 Opening: TV film studio set
│       ├── u2_online_video_lesson.jpg      # Unit 2 Reading: teacher using web videos in class
│       ├── u2_elearning_webcam_student.jpg # Unit 2 Reading: distance learner with webcam
│       ├── u2_science_volcano_clip.jpg     # Unit 2 Reading: volcanic eruption video lesson
│       ├── u2_khan_academy_learning.jpg    # Unit 2 Reading: Khan Academy digital interface
│       ├── u3_pilot_cockpit.jpg            # Unit 3 Opening: commercial airline pilot in cockpit
│       ├── u3_nurse_hospital.jpg           # Unit 3 Opening: nurse in clinical healthcare ward
│       ├── u3_travel_agent.jpg             # Unit 3 Opening: travel agent arranging tourism trips
│       ├── u3_salesperson_store.jpg        # Unit 3 Opening: salesperson in department store
│       ├── u3_carpenter_workshop.jpg       # Unit 3 Opening: carpenter crafting woodwork
│       ├── u3_marine_engineer.jpg          # Unit 3 Opening: marine engineer on ship machinery
│       ├── u3_graphic_designer.jpg         # Unit 3 Pair Work: graphic designer in advertising firm
│       ├── u3_police_officer.jpg           # Unit 3 Pair Work: traffic police officer
│       ├── u3_restaurant_waiter.jpg        # Unit 3 Pair Work: restaurant waiter serving customers
│       ├── u3_reading_saudi_employment.jpg # Unit 3 Reading: Saudi Vision 2030 employment & careers
│       ├── u3_saudi_professionals.jpg      # Unit 3 Reading: young Saudi engineers & physicians
│       ├── u4_youth_leisure_activities.jpg # Unit 4 Opening: leisure preferences of youth
│       ├── u4_videogames_pastime.jpg       # Unit 4 Opening: teenagers playing video games
│       ├── u4_foodcourt_friends.jpg        # Unit 4 Opening: eating lunch in mall food courts
│       ├── u4_indoor_climbing.jpg          # Unit 4 Listening: indoor bouldering and rock climbing
│       ├── u4_cooking_pastime.jpg          # Unit 4 Listening: creative cooking pastime
│       ├── u4_conversation_aerobatics.jpg  # Unit 4 Conversation: stunt flying & aerobatic planes
│       ├── u4_reading_drone_aeromodelling.jpg # Unit 4 Reading: radio-controlled aircraft taking off
│       ├── u4_reading_jet_aeromodel.jpg    # Unit 4 Reading: high-speed jet-turbine scale model
│       ├── u4_football_sports_pastime.jpg  # Unit 4 Workbook: school football team training
│       ├── u4_gym_workout_training.jpg     # Unit 4 Workbook: physical conditioning at fitness gym
│       ├── u5_restaurant_dining_counter.jpg # Unit 5 Opening: restaurant counter with fresh sandwiches & salads
│       ├── u5_food_menu_spread.jpg         # Unit 5 Opening: restaurant menu spread with appetizers & desserts
│       ├── u5_server_taking_order.jpg      # Unit 5 Pair Work: server writing guest's dinner order
│       ├── u5_conversation_ordering_meal.jpg # Unit 5 Conversation: two diners discussing menu selections
│       ├── u5_reading_global_pizza.jpg     # Unit 5 Reading: wood-fired artisan pizza slice
│       ├── u5_reading_global_tacos.jpg     # Unit 5 Reading: Mexican street tacos with cilantro & lime
│       ├── u5_reading_global_sushi.jpg     # Unit 5 Reading: Japanese sushi rolls with salmon & avocado
│       ├── u5_reading_middle_eastern_feast.jpg # Unit 5 Reading: Middle Eastern shawarma & kebab platter
│       ├── u5_cooking_kitchen_pot.jpg      # Unit 5 Writing: chef simmering savory rice in heavy cooking pot
│       ├── u5_gourmet_kabsa_platter.jpg    # Unit 5 Writing: authentic Saudi chicken kabsa platter
│       ├── u6_space_science_museum.jpg     # Unit 6 Opening: space exploration pavilion with rocket models
│       ├── u6_archaeological_museum.jpg    # Unit 6 Opening: archaeological museum hall with stone monuments
│       ├── u6_historic_costumes_exhibit.jpg # Unit 6 Opening: traditional historical costumes display
│       ├── u6_national_heritage_hall.jpg   # Unit 6 Opening: grand marble hall with museum visitors
│       ├── u6_ancient_artifacts_display.jpg # Unit 6 Pair Work: museum glass showcases with ancient pottery
│       ├── u6_museum_tourists_gallery.jpg  # Unit 6 Listening: international museum gallery with tour guide
│       ├── u6_conversation_weekend_visit.jpg # Unit 6 Conversation: two students sharing weekend trip memories
│       ├── u6_reading_islamic_calligraphy.jpg # Unit 6 Reading: historic Qur'anic page in early Kufic script
│       ├── u6_reading_historic_manuscript.jpg # Unit 6 Reading: master calligrapher holding handcrafted reed pen
│       ├── u6_reading_modern_calligraphy_art.jpg # Unit 6 Reading: contemporary artistic Arabic calligraphy canvas
│       └── u6_writing_museum_recount.jpg   # Unit 6 Writing: student writing notes in museum notebook
│
└── Source Reference Documents:
    ├── كتاب الطالب (2).pdf                 # McGraw-Hill Super Goal 2 Student's Book & Workbook
    ├── قاموس مصور -SG2.pdf                 # Super Goal 2 Illustrated Thematic Dictionary
    └── المهارات_المطلوبة_لمادة_اللغة_الإنجليزية.pdf # Ministry of Education Skills Document
```

---

## 5. Phase 3 (Units 5 & 6) Implementation Summary

### Unit 5: *Is There Any Ice Cream?* (Student's Book Pages 44–51)
- **Vocabulary:** 42 official vocabulary items covering food categories, dining verbs, restaurant courses (appetizers, main dishes, desserts, beverages), quantifiers (`some`, `any`, `much`, `many`, `a lot of`, `a few`, `a little`), and culinary partitives (`a cup of`, `a bottle of`, `a slice of`, `a loaf of`, `a bowl of`).
- **Grammar Modules:**
  - **Module 11:** Count vs. Non-Count Nouns, Partitives, and Quantifiers.
  - **Module 12:** Expressions of Desire & Limits: `Would like` vs. `Want` + `Too` vs. `Enough`.
- **Pronunciation Lab 5:** Inflectional Endings of Plural Nouns: Voiceless `/s/`, Voiced `/z/`, and Sibilant `/ɪz/` extra syllable rules.
- **Reading Story 5:** *"The Globalization of Food"* (The universal diffusion of pizza, Mexican tacos, Japanese sushi, and localized culinary adaptations including McDonald's McArabia flatbread sandwich in Saudi Arabia).
- **Writing Task 5:** Traditional Saudi Recipe: Step-by-Step Cooking Guide for Authentic Saudi Chicken Kabsa with exact measurements and transition sequence markers.
- **Discussion Scenarios 13 to 15:**
  - Scenario 13: Ordering Dinner at an Authentic Saudi Restaurant.
  - Scenario 14: Grocery Shopping List & Checking Kitchen Inventory.
  - Scenario 15: Planning a Cultural Food Festival at Intermediate School.
- **Exams 21 & 22:** 40 multiple-choice questions with visual clues and detailed pedagogical explanations.

### Unit 6: *What Was It Like?* (Student's Book Pages 52–59)
- **Vocabulary:** 42 official vocabulary items covering museum pavilions, archaeological antiquities, historical costumes, regular/irregular simple past verbs, and evaluative intensifiers (`so`, `such`).
- **Grammar Modules:**
  - **Module 13:** Simple Past Tense: Regular Verbs (`-ed` inflections) and Common Irregular Verbs (`went, saw, had, took, bought, made`).
  - **Module 14:** Past Tense Questions & Negatives with Auxiliary `Did` + Intensifiers `So` and `Such`.
- **Pronunciation Lab 6:** Simple Past Regular Verb `-ed` Endings: Voiceless `/t/`, Voiced `/d/`, and Stressed Syllable `/ɪd/` rules.
- **Reading Story 6:** *"The Art of the Pen: Arabic Calligraphy"* (The development of the six classical styles: Kufic on ancient Qur'anic parchment, Thuluth on the Saudi national flag and surah headings, Naskh and Ruq'ah for daily manuscripts and printing, and Diwani for royal proclamations).
- **Writing Task 6:** An Unforgettable Journey Through Time: Recount of a Class Excursion to the National Museum of Saudi Arabia in Riyadh.
- **Discussion Scenarios 16 to 18:**
  - Scenario 16: Recounting an Exciting Weekend Excursion to the National Museum.
  - Scenario 17: Inquiring About an Ancient Archaeological Artifact.
  - Scenario 18: Admiring the Saudi National Flag and Calligraphic Inscriptions.
- **Exams 23 & 24:** 40 multiple-choice questions with visual clues and detailed pedagogical explanations.

### Capstone & Midterm Examinations (Exams 25 to 30)
- **Exam 25:** Food & Past Experiences Dual Mastery (Units 5 & 6 Integrated Challenge).
- **Exam 26:** Comprehensive Vocabulary Lexicon Examination (Units 1 to 6).
- **Exam 27:** Master Structural Grammar & Syntax Examination (Units 1 to 6).
- **Exam 28:** Reading Comprehension, Cultural Context & Literature Examination (Units 1 to 6).
- **Exam 29:** Applied Writing, Dialogue Mechanics & Discourse Examination (Units 1 to 6).
- **Exam 30:** Grand All-Star Olympiad & Academic Honors Examination (Units 1 to 6 Comprehensive Finale).

---

## 6. Next Step Blueprint (Phase 4: Units 7 & 8) — الخطوة القادمة

When the user asks to begin **Phase 4 (Units 7 & 8)**, adhere to this curriculum specification:

### Unit 7: *What Happened?* (Student's Book Pages 60–67)
- **Functions:**
  - Reporting past events, personal mishaps, accidental occurrences, and eyewitness accounts.
  - Asking and answering about past continuous activities interrupted by simple past events.
  - Expressing surprise, sympathy, and conversational empathy (`What happened?`, `I'm so sorry to hear that`).
- **Grammar Modules to Add (Modules 15 & 16):**
  - **Module 15:** Past Progressive Tense (`was / were + verb-ing`) for ongoing past activities.
  - **Module 16:** Past Progressive vs. Simple Past with Time Clauses (`while` and `when`).
- **Pronunciation:** Reduced pronunciation of `was` /wəz/ and `were` /wər/ in fast continuous speech.
- **Reading Story 7:** *"Heroic Rescues & Emergency Civil Defense in Saudi Arabia"*.
- **Writing Task 7:** Writing an official accident recount or eyewitness news report.
- **Cultural Images to Extract:** Saudi Civil Defense vehicles, medical emergency response, and road safety awareness.

### Unit 8: *What's Wrong?* (Student's Book Pages 68–75)
- **Functions:**
  - Describing health symptoms, minor illnesses, and physical discomforts.
  - Asking about well-being (`What's wrong?`, `What's the matter?`).
  - Giving medical advice and recommendations using modals `should`, `shouldn't`, and imperative directives.
- **Grammar Modules to Add (Modules 17 & 18):**
  - **Module 17:** Expressing Ailments with `have / has got` + Health symptoms (`a headache`, `a fever`, `a stomachache`).
  - **Module 18:** Modal Auxiliaries for Advice and Recommendation: `Should` vs. `Shouldn't` vs. Imperatives.
- **Pronunciation:** Intonation in sympathetic inquiries and falling pitch in giving advice.
- **Reading Story 8:** *"Healthcare Excellence & Saudi Vision 2030 Wellness"*.
- **Writing Task 8:** Writing a health advisory brochure or doctor-patient dialogue.
- **Cultural Images to Extract:** King Fahad Medical City, modern Saudi clinics, and pharmacy care.

---

## 7. Audio & Speech Architecture (Deepgram American Voice, 75% Speed & Zero-Lag Sync)

- Dedicated Deepgram Voice Studio modal (`#deepgramConfigModal`) in the header.
- Supports premier natural American English models (`aura-asteria-en`, `aura-luna-en`, `aura-orion-en`, `aura-zeus-en`).
- **Speech Speed Control (75% Slow Pace vs 100% Normal Pace):**
  - Prominent speed toggle button in player controls: `🐢 Speed: 75% (Slow)` vs `⚡ Speed: 100% (Normal)`.
  - Persisted in `localStorage ('preferred_speech_rate')`.
  - Applies across all spoken audio: reading stories, vocabulary entries, and discussion scenarios.
- **Zero-Lag Synchronized Highlighting Engine:**
  - Sentence-chained playback architecture with sub-25ms start time.
  - High-frequency animation-frame time synchronization with word timeline matching `audio.currentTime` with 0ms delay at both speeds.
  - Students can click directly on any individual sentence in the passage to hear and follow along.
