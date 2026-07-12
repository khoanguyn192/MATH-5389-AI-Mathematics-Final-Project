# MATH-5389-AI-Mathematics-Final-Project
An Evaluation of Algorithmic Bias and Fragility in Rate My Professor Sentiment Analysis
Course: MATH 5389 - AI Math Final Project

---

# Overview
This project builds a sentiment classifier on real Rate My Professor (RMP) reviews, then deliberately stress tests it. Rather than stopping once the model looks accurate, the project pushes it toward failure through overfitting experiments, adversarial (tricky) examples, and a bias audit. RMP reviews are informal, sarcastic, emotionally driven, and sometimes touch in identity (accent, language, gender). That makes them a good stress test for a classic NLP pipeline built on TF-IDF features and a linear classifier.

---

# Goals

1. Train a baseline sentiment classifier on real data.
2. Show how model complexity (n-grams, regularization strength c) drives a model from underfitting to overfitting.
3. Break the model with adversarial inputs sarcasm, keyword stuffing, and negation.
4. Audit the model for bias by comparing performance on subgroups against the dataset.
5. Produce a 4-6 page report where the model succeeds, where it fails, and why those failures matter.

---

# Project Structure

Introduction: Background on RMP and why sentiment analysis on it is a good test case.
Goals: What the project sets out to demonstrate.
Setup & Data Loading: Imports and loading the real RMP dataset from GitHub.
Dataset Pre-Processing: Filtering placeholders, short comments, mapping raw labels "Awful", "Neutral", "Great", and a word cloud with a vocabulary check.
Training, Testing & Baseline Model: TF-IDF and Logistic Regression pipeline, parameter search, and a regularized baseline model with a confusion matrix.
Overfitting: A complexity sweep to deliberately overfit the model.
Failures: Hand written adversarial reviews (sarcasm, keyword stuffing, negation, backhanded compliments) used towards the baseline and overfit models.
Bias Analysis: Subgroup of reviews that mention accent, language, or gender versus the rest of the data.
References: Important references that were used in this project.

---

# Data
- Source: https://github.com/vxuv/ratemyprofessor-dataset Real RMP reviews, loaded directly from GitHub in the notebook.
- Preprocessing: The 10,000 most recent reviews are used after removing place holder comments and comments under 20 characters.
- Labels: Raw sentiment strings are mapped into three categories: "Awful", "Neutral", and "Great."
Source: https://github.com/vxuv/ratemyprofessor-dataset Real RMP reviews, loaded directly from GitHub in the notebook.
Preprocessing: The 10,000 most recent reviews are used after removing place holder comments and comments under 20 characters.
Labels: Raw sentiment strings are mapped into three categories: "Awful", "Neutral", and "Great."


---

# QuantegyAI — Brand Colors

A quick reference for anyone making slides, docs, graphics, or study materials that need to match the QuantegyAI look. **Copy the hex codes** (the `#` numbers) straight into Canva, Google Slides, PowerPoint, or any design tool.

> **The one-line version:** chrome-and-cyan robot on a deep navy (near-black) background. Bright blue accents, silver text. Never on a plain white background.

---

## The core palette

| Color | Swatch | Hex code | Where it's used |
|---|---|---|---|
| **Electric Cyan** (the signature accent) | 🟦 | `#3DA9FC` | Buttons, links, the "AI" in the logo, robot's eyes, highlights |
| **Bright Blue** (deeper accent) | 🔵 | `#0EA5E9` | Gradients, hover states, glow effects |
| **Deep Navy** (main background) | ⬛ | `#0A0E1A` | Page backgrounds — this is the "dark" everything sits on |
| **Navy Slate** (softer background) | ⬛ | `#0F172A` | Cards, panels, section backgrounds |
| **Soft White** (main text) | ⬜ | `#F1F5F9` | Body text and headings on the dark background |
| **Muted Slate** (secondary text) | ▪️ | `#94A3B8` | Subtitles, captions, less-important text |
| **Chrome Silver** (the robot/logo finish) | ⬜ | `#CFD5DC` → `#7D8893` | The mascot's metallic body and the wordmark — a light-to-dark silver gradient |

---

## How to use them

**Backgrounds → Deep Navy.** Everything is built on the dark navy. Text and color pop against it.

**Accent color → Electric Cyan (`#3DA9FC`).** This is the "QuantegyAI blue." Use it for anything you want to draw the eye to: a button, a key word, an underline, an icon.

**Text → Soft White for the main words, Muted Slate for the quieter ones.** Never pure black text — the whole design lives on dark.

**Gradients → Cyan to Bright Blue** (`#3DA9FC` → `#0EA5E9`) for buttons and glows, or **Silver light-to-dark** (`#CFD5DC` → `#7D8893`) for the metallic/chrome look.

---

## A few rules to keep it on-brand

- ✅ **Dark backgrounds only.** The logo and colors are designed for navy. Putting them on white makes the silver logo disappear.
- ✅ **Keep the robot's eyes cyan.** That blue is the brand — silver/grey eyes make the robot look "switched off."
- ⛔ **Don't use purple.** Older versions of the site had an indigo/purple accent (`#6366F1`, `#A855F7`) — that's **off-brand**. Stick to the cyan/blue family.
- ⛔ **Don't stretch or recolor the logo/mascot.** Scale it evenly.

---

## Fonts (to match)

- **Inter** for everything — body text and headings. It's a free Google Font.
- Big headlines: Inter **Bold** or **Extra-Bold**.
- Tagline style: ALL CAPS, letter-spaced out — like **"LEARN SMARTER. PASS FASTER."**

---

## Quick copy-paste list

```
Electric Cyan   #3DA9FC   (main accent)
Bright Blue     #0EA5E9   (deeper accent / gradients)
Deep Navy       #0A0E1A   (main background)
Navy Slate      #0F172A   (cards / panels)
Soft White      #F1F5F9   (main text)
Muted Slate     #94A3B8   (secondary text)
Chrome Silver   #CFD5DC   (logo highlight)
Chrome Dark     #7D8893   (logo shadow)
```

*Tagline:* **Learn smarter. Pass faster.**
