name: Bug Report
labels: "bug"
description: Report a problem you're having
body:
  - type: checkboxes
    id: terms
    attributes:
      label: Acknowledgements
      options:
        - label: I have checked if my issue has already been reported, and I am certain that my problem has not already been addressed.
          required: true
        - label: I agree that I just checked every box without actually reading anything and that noone needs to fix this.
          required: false
  - type: textarea
    id: what-happened
    attributes:
      label: What problem did you encounter?
      description: |
        Provide a comprehensive description of the problem you're facing.
    validations:
      required: false
