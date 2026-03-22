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

    Content Filters: Rules that trigger based on reports, keywords, or URLs to filter or remove problematic content.

    Auto-Responses: Automated comments to ensure users are aware of subreddit rules and account requirements.

# 🛠 Installation

    Navigate to your subreddit's Mod Tools.

    In the sidebar, find AutoModerator (Mod Tools > Moderation > Automod).

    Copy and paste the entire code block from the configuration file.

    Save the page.
    
# 🚀 Feature Breakdown

## 🛡 Safety & Security

    Doxxing Filter: Uses complex regex to identify and filter email addresses or private contact info. It includes a whitelist for official community emails.

    Threat Filter: Screens for death wishes, calls for violence, and self-harm keywords.

    Report Auto-Filter: Automatically moves any item with 1 report to the Mod Queue for immediate human review.

    Mass Edit Filter: Prevents users from "nuking" their history using third-party scripts (like Redact.dev) which can disrupt community archives.

## 🚫 Spam & Scam Prevention

    T-Shirt/Merch Filter: A massive database of known "Gear" and "Shirt" scam domains.

    Link Shorteners: Blocks over 300+ known link shorteners to prevent users from bypassing domain filters.

    Snapchat/Social Spam: Detects "Add me on Snap" patterns and bot-like behavior.

    Crowdfunding & Petitions: Filters GoFundMe, Change.org, and similar links to prevent unauthorized solicitations.

## ⚖️ Community Standards

    Age/Karma Thresholds: Filters content from accounts less than 7 days old or with less than 50 karma.

    Political Filter: Screens for highly volatile political keywords to keep the community focused on its primary topic.

    Offensive Remarks/Sexual Harassment: Two heavy-duty blocks of keywords and regex to catch slurs, bigotry, and harassment.
