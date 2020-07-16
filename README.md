# Sysdig

Sysdig is a platform for monitoring things. This integration is with their Sysdig monitor platform.


---------

<kbd>
<a href="https://support.xmatters.com/hc/en-us/community/topics">
   <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</a>
</kbd>

---------

# Files

* [Sysdig.zip](Sysdig.zip) - Workflow zip file with the step and example flow
* [sysdig.png](/sysdig.png) - Sysdig logo

# Installation

## xMatters Setup
1. Download the [Sysdig.zip](Sysdig.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Get the URL from the **Inbound from Sysdig** step.
5. Take the Sysdig Monitor API Token and put it into the **Sysdig API Token** constant in xMatters. This value is used in the **Sysdig - Acknowledge Alert** step under the Acknowledge Response.
6. If for some reason your Sysdig instance is hosted somewhere besides Sysdig, the Sysdig Endpoint in xMatters can be changed to point at the API.
7. Update the recipients in the **Create Event** Step.

## Sysdig Setup
This requires an account with Sysdig Monitor.

1. Go to [Account Settings > Notification Channels](https://app.sysdigcloud.com/#/settings/notifications).
2. Click **Add Notification Channel > Webhook**
3. Paste the URL you got from xMatters in the Url field.
4. Call the channel name whatever you'd like (i.e. **xMatters**)
5. Make any other changes you would like and then click **Save**

Now you can add this notification channel to any alerts you would like.

Get your API Key. This is used for sending the acknowledge response back to sysdig.

1. Go to [Account Settings > User Profile](https://app.sysdigcloud.com/#/settings/user)
2. Get your Sysdig Monitor API Token.
3. Copy this and put it in an xMatters constant. (This is later used in the **Sysdig - Acknowledge Response** step)

**Note: as of creating this integration, the API is still in Beta, so it may break at any time.**


## Example
This is an image of the provided flow

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

