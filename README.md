# ThisSideofRylee Automod Code
Created By: ItsNovrix | Version 1.0 (March 2026)

This repository contains an automoderator setup designed to automate content moderation, enhance community safety, and reduce manual moderator workload. It includes advanced regex for threat detection, comprehensive spam site lists, and automated user feedback.

# 📋 Table of Contents

1. Overview

2. Installation

3. Feature Breakdown

4. Safety & Security

5. Spam & Scam Prevention

6. Community Standards

7. Customization Guide

8. Technical Notes

# 📖 Overview

The code is divided into two primary sections:

- Content Filters: Rules that trigger based on reports, keywords, or URLs to filter or remove problematic content.

- Auto-Responses: Automated comments to ensure users are aware of subreddit rules and account requirements.

# 🛠 Installation

- Navigate to your subreddit's Mod Tools.

- In the sidebar, find AutoModerator (Mod Tools > Moderation > Automod).

- Copy and paste the entire code block from the configuration file.

- Save the page.
    
# 🚀 Feature Breakdown

## 🛡 Safety & Security

- Report Auto-Filter: Automatically moves any item with 1 report to the Mod Queue for immediate human review.

- Mass Edit Filter: Prevents users from "nuking" their history using third-party scripts (like Redact.dev) which can disrupt community archives.

- Doxxing Filter: Uses complex regex to identify and filter email addresses or private contact info. It includes a whitelist for official community emails.

- Threat Filter: Screens for death wishes, calls for violence, and self-harm keywords.

## 🚫 Spam & Scam Prevention

- NSFW and Shock Sites Filters: TEXT HERE

- Scam/Spam Sites Filter: TEXT HERE

- T-Shirt/Merch Filter: A massive database of known "Gear" and "Shirt" scam domains.

- Snapchat/Social Spam: Detects "Add me on Snap" patterns and bot-like behavior.

- Crowdfunding & Petitions: Filters GoFundMe, Change.org, and similar links to prevent unauthorized solicitations.

- Petition Sites Filter: TEXT HERE

- Link Shorteners: Blocks over 300+ known link shorteners to prevent users from bypassing domain filters.

## ⚖️ Community Standards

- Tabloid Accounts Filter: TEXT HERE

- Age/Karma Thresholds: Filters content from accounts less than 7 days old or with less than 50 karma.

- Post Length Filter: TEXT HERE

- Political Filter: Screens for highly volatile political keywords to keep the community focused on its primary topic.

- Offensive Remarks/Sexual Harassment: Two heavy-duty blocks of keywords and regex to catch slurs, bigotry, and harassment.

# ⚙️ Customization Guide

## Changing Thresholds

If you find the karma or age requirements too strict or too lenient, locate this section:

```yaml
account_age: "< 7 days"/
combined_karma: "< 50"```

Simply change the numbers to your preferred limits.

## Adding New Keywords

To add a word to the filters (like the Political or Offensive filters), add it to the list inside the brackets:

`["word1", "word2", "your_new_word"]`

Note: Ensure strings are wrapped in double quotes and separated by commas.

## Adjusting Report Sensitivity

The current setting is: `reports: 1.`

- 1 report: High security, but creates more work for mods.

- 2-3 reports: Good for larger communities to prevent a single "troll report" from hiding content.

# ⚠️ Technical Notes

> **Action Logic:** Most rules use action: filter. This means the content is hidden from the public but appears in your Mod Queue for a final "Approve" or "Remove" decision.

> **Regex:** Many rules use Regular Expressions (regex) to catch variations of words (e.g., catching "faggot" and "faggit"). Be careful when editing regex strings, as a missing bracket can break the entire configuration.

> **Stickied Comments:** The Rules Reminder is set to appear on every post as a stickied and locked comment to ensure maximum visibility.
