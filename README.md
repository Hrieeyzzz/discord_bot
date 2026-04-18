<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<style>
@page {{
size: A4;
margin: 20mm;
background-color: #ffffff;
}}
body {{
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
color: #333;
line-height: 1.6;
margin: 0;
padding: 0;
}}
h1 {{
color: #5865F2; /* Discord Blurple */
border-bottom: 2px solid #5865F2;
padding-bottom: 10px;
font-size: 24pt;
}}
h2 {{
color: #2c3e50;
border-left: 5px solid #5865F2;
padding-left: 10px;
margin-top: 30px;
font-size: 18pt;
}}
h3 {{
color: #34495e;
font-size: 14pt;
}}
code {{
background-color: #f4f4f4;
padding: 2px 5px;
border-radius: 3px;
font-family: 'Courier New', Courier, monospace;
}}
pre {{
background-color: #2f3136;
color: #ffffff;
padding: 15px;
border-radius: 8px;
overflow-x: auto;
font-size: 10pt;
}}
table {{
width: 100%;
border-collapse: collapse;
margin-top: 15px;
}}
th, td {{
text-align: left;
padding: 10px;
border-bottom: 1px solid #ddd;
}}
th {{
background-color: #f8f9fa;
}}
.feature-list {{
list-style: none;
padding: 0;
}}
.feature-list li {{
margin-bottom: 10px;
}}
</style>
</head>
<body>
<h1>📢 Broadcast Buddy</h1>
<p>Elevate your community messaging with professional, elegantly formatted announcements. Select a channel, craft your message, and dispatch it with a single, intuitive slash command.</p>

<h2>✨ Features</h2>
<ul class="feature-list">
    <li><strong>🎯 Channel Selector:</strong> Directly pick any text or announcement channel from the Discord client UI.</li>
    <li><strong>🎨 Embed Customization:</strong> Supports headlines, multi-line content, and custom hex color codes (e.g., <code>#FFD700</code>).</li>
    <li><strong>🖼️ Banner Images:</strong> Optionally include a custom image or GIF banner to make your announcements pop.</li>
    <li><strong>🔐 Secure Design:</strong> Restricted to server administrators only via <code>Administrator</code> permissions.</li>
    <li><strong>⚡ Seamless Slash Commands:</strong> No messy prefix commands—all interactions use Discord’s modern built-in interface.</li>
</ul>

<h2>🚀 How to Set Up</h2>
<h3>1. Bot Registration</h3>
<p>Go to the Discord Developer Portal, create a New Application, and generate a Bot Token. Ensure <strong>Message Content Intent</strong> is enabled.</p>

<h3>2. Environment Configuration</h3>
<p>Create a <code>.env</code> file in your root directory:</p>
<pre>DISCORD_TOKEN=your_bot_token_here\nCLIENT_ID=your_application_id_here</pre>

<h3>3. Installation & Running</h3>
<pre># Install dependencies\nnpm install\n\n# Start the bot\nnpm start</pre>

<h2>🛠️ Commands</h2>
<table>
    <tr>
        <th>Option</th>
        <th>Type</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><code>target_channel</code></td>
        <td>Channel</td>
        <td>The channel to send the post to.</td>
    </tr>
    <tr>
        <td><code>headline</code></td>
        <td>String</td>
        <td>The bold title of the embed.</td>
    </tr>
    <tr>
        <td><code>content</code></td>
        <td>String</td>
        <td>The body text (supports \\n).</td>
    </tr>
    <tr>
        <td><code>color</code></td>
        <td>String</td>
        <td>Hex code (e.g., #7289da).</td>
    </tr>
</table>

<h2>📂 Project Structure</h2>
<pre>
├── src/
│   ├── commands/      # Command logic
│   └── index.js       # Main entry point
├── .env               # Secrets
└── package.json       # Metadata
</pre>

</body>
</html>
"""

with open("README.html", "w") as f:
f.write(html_content)

HTML(filename="README.html").write_pdf("Broadcast_Buddy_README.pdf")

Your professional project documentation is ready. I have generated a comprehensive `README.md` file along with a polished PDF version for your records.

### Your README includes:
- **Feature Highlights:** Detailed breakdown of the bot's capabilities.
- **Setup Guide:** Step-by-step instructions from the Discord Developer Portal to local environment configuration.
- **Command Documentation:** A clear table outlining the `/announce` parameters.
- **Project Architecture:** A visual map of the source directory and configuration files.
- **Security Context:** Explanation of the administrative restrictions applied to the slash commands.

Your files are ready for download below:

[file-tag: code-generated-file-2-1776498040180643648]
[file-tag: code-generated-file-0-1776498040180635748]
