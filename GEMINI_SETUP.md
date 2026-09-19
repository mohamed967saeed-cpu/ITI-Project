# Gemini AI setup

The dashboard now includes **AI Smart Restock** and **AI Sales Insights**. The AI receives only the calculated inventory/sales facts needed for the report.

Google's Gemini API uses an `x-goog-api-key` header for REST requests. Do not commit your API key to source control.

## Windows PowerShell

Set the key for your user account:

```powershell
[Environment]::SetEnvironmentVariable("GEMINI_API_KEY", "YOUR_KEY_HERE", "User")
```

Restart Visual Studio after setting it.

## Alternative: ASP.NET user secrets

From the project folder:

```powershell
dotnet user-secrets init
dotnet user-secrets set "Gemini:ApiKey" "YOUR_KEY_HERE"
```

The model can be changed in `appsettings.json` under `Gemini:Model`.

The current default is `gemini-3.6-flash`.
