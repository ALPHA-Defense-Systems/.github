name: Weekly Training Task
description: Track a single SOC Tier 1 weekly challenge
title: "[Week ##] TASK TITLE"
labels: ["training", "week", "soc-tier1"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        ## 🧠 SOC Tier 1 Training - Weekly Challenge

  - type: input
    id: week-number
    attributes:
      label: 📅 Week Number
      description: Enter the week number (e.g., 01, 12, etc.)
      placeholder: "01"
    validations:
      required: true

  - type: input
    id: platform
    attributes:
      label: 🔗 Platform
      description: Where is the challenge hosted?
      placeholder: "HTB Academy / CyberDefenders / TryHackMe / BTLO"
    validations:
      required: true

  - type: input
    id: challenge-name
    attributes:
      label: 🏁 Challenge / Module Name
      placeholder: "Linux Fundamentals"
    validations:
      required: true

  - type: input
    id: challenge-link
    attributes:
      label: 🌐 Challenge URL
      placeholder: "https://..."
    validations:
      required: true

  - type: dropdown
    id: category
    attributes:
      label: 🧩 Skill Focus
      options:
        - DFIR
        - Windows Logs
        - Networking
        - Threat Hunting
        - Malware Analysis
        - Detection Engineering
        - AD Analysis
        - Red Team Awareness
        - Log Analysis
        - Reporting
        - SIEM
        - Other
    validations:
      required: true

  - type: textarea
    id: deliverable
    attributes:
      label: ✅ Expected Deliverable
      description: What should the analyst submit (e.g., IOC list, report, notes)?
      placeholder: "Submit a markdown writeup with key takeaways and 3 detection rules..."
    validations:
      required: true

  - type: textarea
    id: notes
    attributes:
      label: 💬 Additional Notes
      description: Any extra guidance or walkthrough hints
      placeholder: "Focus on process creation events and correlation with Sysmon logs..."
    validations:
      required: false
