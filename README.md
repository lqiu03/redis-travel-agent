# 🌍 Autogen Travel Concierge 

A sophisticated AI travel planning assistant showcasing AutoGen's advanced memory capabilities with dual-layer memory architecture: Redis-backed chat history and Task-Centric Memory (TCM) for intelligent learning.

## 🧠 What's included?

- **🎯 Dual-Layer Memory**: Short-term chat history (Redis) + Long-term learning (TCM)
- **👥 User Isolation**: Pre-seeded users get completely separate memory contexts
- **🔄 Session Persistence**: Your conversations and preferences survive app restarts
- **📚 Intelligent Learning**: The agent learns your travel preferences automatically
- **🌐 Real-time Search**: Live travel information via Tavily search API
- **💬 Clean Chat UI**: Gradio interface with user management

## 🚀 Quick Setup (<5 minutes)

### Step 1: Get Your API Keys
You'll need three API keys:
- **OpenAI API Key**: Get from [platform.openai.com](https://platform.openai.com/api-keys)
- **Tavily API Key**: Get from [tavily.com](https://tavily.com) (free tier available)  
- **Redis URL**: For chat history storage (see Step 2)

### Step 2: Set Up Redis
You have 3 options for Redis:

#### Option A: Local Redis with Docker**
```bash
docker run --name redis -p 6379:6379 -d redis:8.0.3
```

#### Option B: Redis Cloud
Get a free db [here](https://redis.io/cloud).

#### Option C: Azure Managed Redis
Here's a quickstart guide to create Azure Managed Redis for as low as $12 monthly: https://learn.microsoft.com/en-us/azure/redis/quickstart-create-managed-redis

### Step 3: Setup the Project
```bash
# Install uv (Python package manager)
curl -LsSf https://astral.sh/uv/install.sh | sh

# Clone and install
git clone <repository-url>
cd amr-autogen-travel-agent

# Get uv env setup
uv sync
```

### Step 4: Configure Your Environment
Create a `.env` file with your API keys:
```bash
cp env.example .env
```

Edit the `.env` file as needed.

### Step 5: Launch the Application
```bash
uv run python gradio_app.py
```

🎉 **Open [http://localhost:7860](http://localhost:7860)** to start chatting!

The application will:
- ✅ Validate your configuration and API connections
- ✅ Initialize the dual-layer memory system
- ✅ Load the user management interface

## 👤 User Profile Configuration

The demo comes with pre-configured user profiles (Tyler and Amanda) that have distinct travel preferences. You can easily customize these or add new profiles by editing `context/seed.json`.

### Current Profiles

**Tyler** 🎒 *The Adventure Eco-Warrior*
- Budget-friendly backpacking and extreme sports enthusiast
- Passionate about sustainable travel and environmental conservation

**Amanda** 🏨 *The Luxury Culture Connoisseur*
- Premium experiences with five-star accommodations and fine dining
- Art, culture, and history enthusiast who loves museums and guided tours

---

**🚀 Ready to see AI memory in action? Start chatting and watch your travel preferences get smarter!**
