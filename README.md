# Agents at Work - Quick Setup

## Install 
```bash
# Install uv
curl -sSf https://astral.sh/uv/install.sh | bash

# Clone repo (if not already done)
git clone https://github.com/Fewsats/agents-at-work.git
cd agents-at-work

# Create virtual environment
uv venv
source .venv/bin/activate

# Install dependencies
uv sync
```

## Adding a New Podcast Episode
```bash
# Activate environment (if not already active)
source .venv/bin/activate

# Add new episode with this format:
python agents_at_work/core.py "YOUTUBE_URL" "[GUEST_NAME](GUEST_LINK)" "TITLE @ [COMPANY](COMPANY_LINK)"
```

### Example
```bash
python agents_at_work/core.py "https://youtu.be/example" "[Jane Doe](https://twitter.com/janedoe)" "CTO @ [AI Company](https://aicompany.com)"
```

**IMPORTANT: After adding a new episode, copy your command to the top of CHANGELOG.md to maintain episode history.**

Links in `[]()` format will become clickable on the website. The script automatically:
- Extracts the transcript
- Generates an AI agent definition
- Updates the consensus definition
- Adds everything to the website

## Tracking Added Episodes

After adding a new episode, copy the exact command you used and add it to the CHANGELOG.md file to keep track of all episodes. This helps maintain a history of all podcast episodes processed by the system.

```bash
# Add your command to the top of CHANGELOG.md
echo 'python agents_at_work/core.py "YOUTUBE_URL" "[GUEST_NAME](GUEST_LINK)" "TITLE @ [COMPANY](COMPANY_LINK)"' >> CHANGELOG.md
```

The CHANGELOG.md serves as a record of all episodes that have been processed by the system.

