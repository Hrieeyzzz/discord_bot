from weasyprint import HTML

# 1. Define the HTML template with CSS
# Note: Double curly braces {{ }} are used in the CSS so Python f-strings don't confuse them with variables
html_content = f"""
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
            white-space: pre-wrap;
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
    <p>Elevate your community messaging with professional, elegantly formatted announcements.</p>

    <h2>✨ Features</h2>
    <ul class="feature-list">
        <li><strong>🎯 Channel Selector:</strong> Directly pick channels from the Discord UI.</li>
        <li><strong>🎨 Embed Customization:</strong> Supports headlines and custom hex colors.</li>
        <li><strong>🖼️ Banner Images:</strong> Include image/GIF banners.</li>
        <li><strong>🔐 Secure Design:</strong> Restricted to administrators.</li>
    </ul>

    <h2>🚀 How to Set Up</h2>
    <h3>1. Bot Registration</h3>
    <p>Go to the Discord Developer Portal and generate a Bot Token. Enable <b>Message Content Intent</b>.</p>

    <h3>2. Environment Configuration</h3>
    <pre>DISCORD_TOKEN=your_token_here\nCLIENT_ID=your_id_here</pre>

    <h2>🛠️ Commands</h2>
    <table>
        <tr><th>Option</th><th>Type</th><th>Description</th></tr>
        <tr><td><code>target_channel</code></td><td>Channel</td><td>Channel destination.</td></tr>
        <tr><td><code>headline</code></td><td>String</td><td>Embed title.</td></tr>
    </table>
</body>
</html>
"""

# 2. Save the HTML to a file
with open("README.html", "w", encoding="utf-8") as f:
    f.write(html_content)

# 3. Generate the PDF
try:
    HTML(string=html_content).write_pdf("Broadcast_Buddy_README.pdf")
    print("Successfully created README.html and Broadcast_Buddy_README.pdf")
except Exception as e:
    print(f"Error generating PDF: {e}")
