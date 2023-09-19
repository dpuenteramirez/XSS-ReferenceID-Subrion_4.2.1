# XSS in Reference ID in Subrion 4.2.1

**Software link**: Subrion CMS 4.2.1 [https://subrion.org/download/]

**@author**: Daniel Puente

**@description**: Cross-site scripting (XSS) vulnerability in `Reference ID` from the panel `Transactions`,  of Subrion v4.2.1 allow attackers to execute arbitrary web scripts or HTML via a crafted payload injected into 'Reference ID' parameter.

---
# PoC

1. A transcation is added into the system, and in the `Reference ID` input, a crafted payload is given.
![transcations XSS](https://github.com/dpuenteramirez/XSS-ReferenceID-Subrion_4.2.1/assets/74184545/21c2650a-1d30-484a-b289-3856d392196e)

2. When the user navigates to `/profile/funds/` the cratted payload is executed.
![funds XSS](https://github.com/dpuenteramirez/XSS-ReferenceID-Subrion_4.2.1/assets/74184545/473083e4-e200-43f5-bb6e-4fcd6ffb6f59)
