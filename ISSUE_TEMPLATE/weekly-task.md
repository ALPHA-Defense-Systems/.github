name: Weekly Training Task
about: Log and track a single SOC Tier 1 weekly training challenge
title: "[Week ##] TASK TITLE"
labels: ["training", "week", "soc-tier1"]
assignees: []
body:
  - type: markdown
    attributes:
      value: |
        ## 🧠 SOC Tier 1 Training – Weekly Challenge Log

        Fill out the following details to track the progress of your weekly SOC challenge.

  - type: input
    id: week-number
    attributes:
      label: 📅 Week Number
      description: Enter the week number (01 to 24)
      placeholder: "01"
    validations:
      required: true

  - type: input
    id: platform
    attributes:
      label: 🔗 Platform
      description: The platform hosting this challenge or module
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
      description: What is the primary area this task covers?
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
      description: What should the analyst submit (writeup, screenshots, IOCs, etc.)
      placeholder: "Submit a markdown writeup with key takeaways, screenshots, and detection rules..."
    validations:
      required: true

  - type: textarea
    id: notes
    attributes:
      label: 💬 Additional Notes
      description: Optional hints or guidance for this challenge
      placeholder: "Focus on process creation events and correlation with Sysmon logs..."
    validations:
      required: false
