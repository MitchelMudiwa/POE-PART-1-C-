# POE-PART-1-C-
CybersecurityBot
A console-based cybersecurity awareness chatbot built with C# and .NET 10. It educates users on common cybersecurity topics through an interactive chat interface.
 Features
	•	 Interactive chatbot with typewriter text effect
	•	 Optional WAV audio greeting on startup
	•	 Colored console output for better readability
	•	 Covers key cybersecurity topics including:
	•	Password safety
	•	Phishing
	•	Safe browsing
	•	Two-factor authentication (2FA)
	•	Malware
	•	Ransomware
	•	Social engineering
    Requirements
	•	.NET 10 SDK
	•	Windows (for audio playback optional)
  Getting Started
1. Clone or download the project
2. git clone https://github.com/yourusername/CybersecurityBot.git
cd CybersecurityBot
2. Build and run
3. dotnet run
4.  Project Structure
5.  CybersecurityBot/
├── CybersecurityBot.csproj   # Project configuration
├── Program.cs                # Entry point
├── User.cs                   # User model
├── AudioManager.cs           # Handles WAV audio greeting
├── ResponseEngine.cs         # Keyword-based response logic
├── DisplayManager.cs         # Console output and formatting
└── Chatbot.cs                # Main chat loop and logic
Usage
When you run the bot it will:
	1.	Play an audio greeting (if greeting.wav is present)
	2.	Display the ASCII art header
	3.	Ask for your name
	4.	Enter the chat loop
Available commands:
Audio Setup (Optional)
To enable the voice greeting:
	1.	Place a file named greeting.wav in the project root
	2.	On build it will be copied to the output folder automatically
	3.	Audio only plays on Windows — other platforms skip it gracefully
To auto-copy the WAV on build, add this to your .csproj:
Command              Description
--------------------------------------------------
help                 Show list of available topics
password             Password safety tips
phishing             How to spot phishing attacks
browsing             Safe browsing practices
2fa / two-factor     Two-factor authentication info
malware              Malware protection tips
ransomware           Ransomware prevention
social engineering   Social engineering awareness
exit                 Quit the bot
<ItemGroup>
  <Content Include="greeting.wav">
    <CopyToOutputDirectory>PreserveNewest</CopyToOutputDirectory>
  </Content>
</ItemGroup>
  Built With
	•	C# 13
	•	.NET 10
	•	System.Media.SoundPlayer (Windows audio)
	•	System.Runtime.InteropServices (platform detection)
  License
This project is open source and free to use for educational purposes.
Author
Made by Mitchel Saule feel free to extend the bot with more topics or an AI-powered response engine!
