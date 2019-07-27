# Splunk-Microsoft-Teams-Webhook-Connector
This is a modified version of the "Microsoft Teams Webhook Alert Connector" from SplunkBase containing code fixes and proxy support.
The original app can be found here: https://splunkbase.splunk.com/app/3375/

This app also incorporates code modifications discussed in Lisa Rushworth's blog here: https://www.rushworth.us/lisa/?tag=splunk 

Usage:
- Download the Microsoft-Teams-Webhook-Connector.tgz file and install it in Splunk
- Set an alert in Splunk and choose the Microsoft Teams action from the alert dropdown
- Enter the Microsoft Teams Inbound Webhook Connector URL as Desired

Proxy Configuration:
If you wish to use a proxy, uncomment the following three lines in /etc/apps/alert_msteams/bin/teams.py and modify the proxy ip and port to suit your environment.

#proxy = urllib2.ProxyHandler({'https': 'https://proxyip:port'})
#opener = urllib2.build_opener(proxy)
#urllib2.install_opener(opener)

Debugging:

Search for index=_internal action=teams
