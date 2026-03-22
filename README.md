# ThisSideofRylee Automod Code
Created By: ItsNovrix | Version 1.0 (March 2026)

This repository contains an automoderator setup created for r/mangionetrials to automate content moderation, enhance community safety, and reduce manual moderator workload. It includes advanced regex for threat detection, offensive terms, comprehensive spam site lists, and other common areas of concern on Reddit.

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

- NSFW and Shock Sites Filters: Screens submissions against a list of known shock sites and major NSFW/Adult domains.

- Scam/Spam Sites Filter: Includes over 100+ known predatory scam/spam domains.

- T-Shirt Spam Filter: A database of common t-shirt scam domains.

- Snapchat Spam Filter: Detects and filters Snapchat spam comments.

- Crowdfunding & Petitions: Filters links from major petition platforms like GoFundMe, Change.org, and similar links.

- Link Shorteners: Blocks over 300+ known link shorteners to prevent users from bypassing domain filters.

## ⚖️ Community Standards

- Tabloid Accounts Filter: Filters submissions from tabloid accounts for manual review. 

- Age/Karma Thresholds: Filters content from accounts less than 7 days old or with less than 50 karma.

- Post Length Filter: Any text submission with a body shorter than 20 characters is automatically filtered.

- Political Filter: Screens for highly volatile political keywords to keep the community focused on its primary topic.

- Offensive Remarks/Sexual Harassment: Two heavy-duty blocks of keywords and regex to catch slurs, bigotry, and harassment.

# ⚙️ Customization Guide

## Changing Thresholds

If you find the age/karma or body text length requirements too strict or too lenient, locate the relevant sections and simply change the numbers to your preferred limits. 

Age/Karma Limit
```yaml
account_age: "< 7 days"
combined_karma: "< 50"
```

Post Length Limit
```yaml
type: text submission
body_shorter_than: 20
```

## Adding New Keywords

To add a new word or phrase to filters like the Political filter or NSFW sites filter, simply add the desired term(s) to the list inside the brackets:

`["word1", "word2", "your_new_word"]`

Note: Ensure format is followed! If a string of words/phrases uses symbols such as quotation marks and commas, make sure to follow the same format when adding new words/phrases.

## Adjusting Report Sensitivity

The current setting is: `reports: 1.`

- 1 report: High security, but can create more work for mods.

- 2-3 reports: Good for larger communities to prevent a single "troll report" from hiding content.

# ⚠️ Technical Notes

> **Action Logic:** Most rules use `action: filter` to handle scenarios. This means the content is hidden from the public but appears in your Mod Queue for a final "Approve" or "Remove" decision.

> **Regex:** Many rules use Regular Expressions (regex) to catch variations of words (e.g., catching "faggot" and "faggit"). Be careful when editing regex strings, as something as small as a missing bracket or comma can break the entire configuration.

> **Rules Reminder Comment:** The Rules Reminder comment is set to appear on every post as a stickied and locked comment to ensure maximum visibility. The comment also includes a direct link to Reddit's Content Policy.

# Need Help?

If you require any additional assistance or customization of this Automod code in the future, feel free to reach out to [u/BravoFive141](https://www.reddit.com/user/BravoFive141/) on Reddit.
