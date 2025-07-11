# 🚀 Apaleo MCP Tools Documentation

**Complete documentation for all Apaleo Model Context Protocol (MCP) tools.**

**Total Tools Available:** 227

---

## 🎯 What is this?

**Apaleo MCP Tools** provide AI assistants (like Claude, ChatGPT, etc.) with direct access to the **Apaleo Hotel Management System**. This means your AI can help you manage bookings, check availability, handle finances, and much more - all through natural conversation!

### 🤖 What is MCP (Model Context Protocol)?

MCP is a standard that allows AI assistants to connect to external systems and tools. Think of it as giving your AI "superpowers" to interact with real hotel software.

**Popular AI assistants that support MCP:**
- **Claude Desktop** (by Anthropic)
- **Cursor IDE** (for developers)
- **Custom integrations** via the MCP protocol

---

## 🏨 What can you do with these tools?

### 📋 **Booking Management**
- Create and modify reservations
- Manage group bookings
- Handle room blocks
- Process offers and pricing

### 💰 **Financial Operations**
- Manage guest folios
- Process payments and refunds
- Generate invoices
- Track revenue and reporting

### 🏢 **Property Management**
- Check room availability
- Manage units and unit groups
- Handle maintenance tasks
- Configure property settings

### 📊 **Analytics & Reporting**
- Generate business reports
- Access system logs
- Track performance metrics

---

## 🚀 Quick Start Guide

### 1. **Get Your Apaleo API Credentials**

Before you can connect any AI assistant to Apaleo, you need API credentials:

#### **Step 1: Create Developer Account**
1. Visit [apaleo.dev](https://apaleo.dev/) 
2. Click **"Create Dev Account"** (it's free!)
3. Complete the registration process

#### **Step 2: Register Your Application**
1. In your developer account, click **"Register an app"**
2. Choose **"OAuth simple client (custom) app"** for MCP usage
3. Fill out the application details:
   - **Name:** "My Hotel MCP Integration" 
   - **Description:** "MCP server for AI assistant integration"
   - **Redirect URIs:** Can be left empty for MCP
4. Submit your application

#### **Step 3: Get Your Credentials**
After registration, you'll receive:
- ✅ **Client ID** (e.g., `SDXE-AC-MYAPP`)
- ✅ **Client Secret** (e.g., `ZiEWFgFeSP...5yhTgsZgx`)

**⚠️ Keep these secure!** You'll need them for authentication.

---

### 2. **Choose Your AI Assistant**

#### **Option A: Claude Desktop (Recommended for End Users)**

**Setup Instructions:**
1. **Download Claude Desktop** from [claude.ai/desktop](https://claude.ai/desktop)
2. **Open Settings:** Claude → Settings → Developer → Edit Config
3. **Configure MCP Server:** Add this to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "apaleo": {
      "command": "npx",
      "args": [
        "-y", 
        "apaleo-mcp-server"
      ],
      "env": {
        "APALEO_CLIENT_ID": "your-client-id-here",
        "APALEO_CLIENT_SECRET": "your-client-secret-here"
      }
    }
  }
}
```

4. **Restart Claude Desktop**
5. **Start chatting:** Look for the 🔨 tool icon in your chat interface!

**📖 Need help with Claude setup?** Check the [official MCP guide](https://docs.anthropic.com/en/docs/build-with-claude/tool-use)

#### **Option B: n8n Workflow Automation (For Advanced Users)**

Perfect for automating hotel operations with AI!

**📥 Get the n8n Workflow Template:**

**Option A: Download File**
- [**n8n_Example_Apaleo_MCP.json**](./n8n_Example_Apaleo_MCP.json) ⬇️ *(Right-click → Save As)*

**Option B: Copy & Paste** 
1. Create a new file called `apaleo_workflow.json`
2. Copy the JSON content from [here](./n8n_Example_Apaleo_MCP.json)
3. Save and import into n8n

**Setup Instructions:**
1. **Install n8n:** Visit [n8n.io](https://n8n.io/) and set up your instance
2. **Import Workflow:** Upload the downloaded JSON file
3. **Configure Credentials:**
   - Add your **Apaleo Client ID & Secret**
   - Add your **OpenAI API Key** 
   - Set the **MCP Server URL** (contact your system administrator)
4. **Test the Workflow:** Send a test message to see AI-powered hotel automation!

**🎯 What the n8n Template Includes:**
- **Chat Interface** with memory
- **OpenAI GPT-4** integration  
- **13+ Essential Tools** (ListProperties, CountUnits, GetAvailableUnits, etc.)
- **Automatic Authentication** token management
- **Ready-to-customize** for your specific needs

#### **Option C: Cursor IDE (For Developers)**

**Setup Instructions:**
1. **Download Cursor** from [cursor.sh](https://cursor.sh/)
2. **Configure MCP:** Use the same configuration as Claude Desktop
3. **Start coding:** Use AI assistance for hotel management scripts and integrations

---

### 3. **Start Using Natural Language**

Once connected, you can interact with your hotel systems naturally:

#### **🏨 Booking Management**
> *"Show me all available rooms for next weekend"*
> 
> *"Create a reservation for John Smith, 2 adults, arriving March 15th"*
> 
> *"What group bookings do we have this month?"*

#### **💰 Financial Operations**
> *"What's the revenue for this month?"*
> 
> *"Show me all unpaid invoices"*
> 
> *"Process a payment for reservation #12345"*

#### **🏢 Property Management**
> *"Check the maintenance status of room 205"*
> 
> *"List all out-of-order units"*
> 
> *"What's our occupancy rate for next week?"*

#### **📊 Reports & Analytics**
> *"Generate a revenue report for last quarter"*
> 
> *"Show me booking trends for the summer season"*
> 
> *"What are our most popular room types?"*

---

### 4. **Troubleshooting**

#### **Common Issues:**

**🔐 Authentication Errors:**
- ✅ Verify your Client ID and Secret are correct
- ✅ Check if your developer account has proper permissions
- ✅ Ensure your application is registered correctly

**🔌 Connection Problems:**
- ✅ Restart your AI assistant after configuration changes  
- ✅ Check your internet connection
- ✅ Verify the MCP server URL is accessible

**❌ "Tool not found" Errors:**
- ✅ Make sure the MCP server is running
- ✅ Check that your configuration file syntax is correct
- ✅ Verify you have permissions for the specific operations

**💬 Need More Help?**
- **Technical Support:** Contact your system administrator
- **API Questions:** Visit [community.apaleo.com](https://community.apaleo.com/c/devs)
- **MCP Issues:** Check [MCP troubleshooting guide](https://modelcontextprotocol.io/docs/troubleshooting)

---

## 🔗 Useful Links

### 📚 **Learn More About MCP**
- [Model Context Protocol Documentation](https://modelcontextprotocol.io/)
- [MCP Servers Hub](https://github.com/modelcontextprotocol/servers)
- [Anthropic MCP Announcement](https://www.anthropic.com/news/model-context-protocol)

### 🏨 **Apaleo Resources**
- [Apaleo Developer Portal](https://apaleo.dev/)
- [Apaleo API Documentation](https://api.apaleo.com/)
- [Apaleo Agent Hub](https://www.apaleo.com/marketplace/)

### 💬 **Community & Support**
- [MCP Discord Community](https://discord.gg/modelcontextprotocol)
- [Apaleo Community](https://community.apaleo.com/)
- [GitHub Discussions](https://github.com/modelcontextprotocol/servers/discussions)

---

## 📚 Documentation Sections

- **📋 Booking Tools** - 45 tools
- **📅 Availability Tools** - 5 tools
- **🏢 Inventory Tools** - 32 tools
- **💰 Finance Tools** - 60 tools
- **💵 Rate Plan Tools** - 35 tools
- **📊 Reports Tools** - 5 tools
- **⚙️ Settings Tools** - 28 tools
- **🔧 Operations Tools** - 10 tools
- **📝 Logs Tools** - 4 tools

---

## 🔧 How to Use This Documentation

### 📖 **For End Users**
1. **Browse by category** - Find tools for your specific needs
2. **Read tool descriptions** - Understand what each tool does
3. **Check required parameters** - See what information you need to provide
4. **Ask your AI naturally** - No need to memorize exact syntax!

### 💻 **For Developers**
- Each tool shows the **exact API endpoint** and **HTTP method**
- **Parameter types** and **requirements** are clearly marked
- **Integration examples** available in the MCP documentation

### 🎯 **Example Usage**

Instead of learning complex API calls, just tell your AI:

**❌ Complex:** 
```
POST /booking/v1/bookings
{"arrival": "2024-03-15", "departure": "2024-03-17", ...}
```

**✅ Simple:**
> *"Book room 205 for Sarah Johnson from March 15-17, 2 guests"*

---

## ⚠️ Important Notes

- **Authentication required:** All tools require valid Apaleo API credentials
- **Permissions matter:** Your AI can only perform actions you're authorized for
- **Real operations:** These tools interact with live hotel data - use carefully
- **Rate limits apply:** Some operations may have usage restrictions

---

## 📞 Need Help?

- **Technical issues:** Check the [MCP troubleshooting guide](https://modelcontextprotocol.io/docs/troubleshooting)
- **Apaleo questions:** Contact [Apaleo support](https://www.apaleo.com/support/)
- **Feature requests:** Join the [community discussions](https://github.com/modelcontextprotocol/servers/discussions)

**Happy hoteling with AI! 🏨✨**
