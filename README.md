# gemini-cli-studybuddy

A custom system prompt configuration for the Gemini CLI that transforms it into an intelligent study buddy for coding challenges.

## Overview

This project contains a system prompt (`gemini-prompt.md`) that configures the Gemini CLI to act as a helpful study buddy for:

- **LeetCode problems** - Guide you through algorithms and data structures
- **Advent of Code puzzles** - Help parse puzzles and structure solutions
- **General coding challenges** - Teach problem-solving techniques

### Key Features

- **Socratic Learning** - Guides you toward answers rather than giving direct solutions
- **Incremental Hints** - Provides hints that escalate based on your progress
- **Encouraging Tone** - Patient and supportive learning environment
- **Concept Teaching** - Explains underlying algorithms and patterns

## Usage

### 1. Set the Environment Variable

Export the path to the `gemini-prompt.md` file:

```sh
export GEMINI_SYSTEM_MD="~/Documents/gemini-cli-studybuddy/gemini-prompt.md"
```

> **Tip:** Add this line to your shell configuration file (e.g., `~/.zshrc`, `~/.bashrc`) to make it persistent across sessions.

### 2. Run Gemini CLI

Start an interactive session:

```sh
gemini
```

Or run a specific prompt:

```sh
gemini "Help me with Two Sum problem from LeetCode"
```

## Example Session

```sh
$ gemini "I'm stuck on LeetCode 1: Two Sum"

# Gemini CLI (Study Buddy Mode)
# ─────────────────────────────────
# Problem: Two Sum
#
# Give it a try! Here are some guiding questions:
#
# - Have you considered what data structure might help
#   you track numbers you've already seen?
# - Think about what happens when you iterate through
#   the array once...
#
# Remember: I won't give you the answer directly.
# Let's work through this together! 🚀
```

## Interaction Guidelines

When the study buddy mode is active, Gemini will:

- ✅ Ask guiding questions to help you think through problems
- ✅ Provide small hints when you're stuck (escalating as needed)
- ✅ Explain algorithms and data structures
- ✅ Help debug your code through questioning
- ✅ Celebrate your progress and solutions

- ❌ Never give you the complete solution upfront
- ❌ Never skip the learning process
- ❌ Never reveal key insights prematurely

## Hint Escalation

If you're stuck, the study buddy follows this pattern:

1. **Conceptual** - "This problem might benefit from a greedy approach."
2. **Directional** - "Consider using a hash map for O(1) lookup."
3. **Implementation** - "You could use a sliding window technique..."
4. **Near-Solution** - Only after significant effort, partial code to unlock progress.

## Asking for Optimized Solutions

Once you've solved a problem yourself, you can ask:

- "Can you show me a better way?"
- "What's the optimal solution?"
- "How can I improve the time complexity?"

The study buddy will then explain alternative approaches with complexity analysis.
