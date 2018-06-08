# Manage Whitelist in exchnage 2013

1. Open Powershell in you server Exchnage
2. `get-ContentFilterConfig`  [find the line **"Bypass Sender Domain"** and **"Bypass Sender"** to view you actual whitelist]
3. `Set-ContentFilterConfig -BypassedSenderDomains microsoft.com,woshub.com,gmail.com` [To add domain in whitelist]
4. `Set-ContentFilterConfig -BypassedSenders jkarlin@gmail.com`  [to add sender in whitelist]
5. `Set-ContentFilterConfig -BypassedSenderDomains @{Remove="gmail.com"}` [to remove a domain added]