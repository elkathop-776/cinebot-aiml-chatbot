# **Cinebot - AIML Conversational Cinema Assistant**

Cinebot is an **AIML 2.0 (Artificial Intelligence Markup Language)** conversational chatbot designed to streamline cinema customer service. It enables users to explore movie schedules, retrieve showtimes, book tickets, and inquire about ticket pricing through an interactive chat interface.
*Developed for the *Conversational Agents* course at Aristotle University of Thessaloniki*

## Key Capabilities
- **Schedule & Showtimes:** Provides active movie listings and specific daily screening times.
- **Ticket Booking:** Interactive multi-turn ticket reservation flow with real-time input validation (restricting ticket count to valid ranges).
- **Proactive Upselling:** Recommends special concession packages (e.g., Popcorn Combos, Family Deals) prior to booking confirmation.
- **External Links:** Direct integration with trailer links and IMDb movie info.
- **Fallback & Human Transfer:** Smooth error handling (`*` matching) for out-of-scope queries with options to retry or escalate to a human agent.

## Project Structure
```text
cinebot/
├── aiml/                # Core conversational patterns and topic flows
│   ├── topics.aiml      # Context-specific logic (Schedule, Booking, Upselling)
│   └── udc.aiml         # Universal Default Categories (Fallback & Damage Control)
├── sets/                # Pattern sets for input classification (greetings, cancel, etc.)
├── maps/                # Key-value lookup tables for dynamic data (movie times)
└── config/              # Properties, normalizations, and substitutions
```
## AIML Architecture & Features
This bot demonstrates core conversational design principles using native AIML 2.0 tags:
- **Context Management (*topic* & *that*):** Tracks multi-turn conversational states during the booking process to keep user interactions natural.
- **Dynamic Lookups (*map* & *set*):** Uses structured pattern sets and dynamic mapping for movie schedules and trigger words.
- **Rich Media & Postback Buttons:** Employs *button*, *link*, and *postback* elements for interactive UI navigation.

## Conversation Example
**User:** Hi there!  
**Bot:** Hello! Welcome to Cinebot. How can I assist you today?  
*`[Show Schedule]` `[Book Tickets]` `[Prices]`*

**User:** Book Tickets  
**Bot:** Which movie would you like to book tickets for?

**User:** Dune Part Two  
**Bot:** Great choice! How many tickets would you like to book (1-10)?

**User:** 2  
**Bot:** Got it! 2 tickets for Dune Part Two. Before we confirm, would you like to add a Popcorn Combo for 10% off?

## How to Run / Test
1. Clone this repository: [cinebot-aiml-chatbot.git](https://github.com/elkathop-776/cinebot-aiml-chatbot.git)
2. Load the project folder into your preferred AIML 2.0 engine or editor (e.g., Program O, Pandorabots, or a local Python program-y interpreter).
3. Load cinebot.properties first, followed by the .set, .map, and .aiml files.

## Author
Elpida Anthopoulou

Institution: Aristotle University of Thessaloniki

Course: Conversational Agents
