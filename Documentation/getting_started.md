# Getting Started

### About SharpCord

is an event based library.

Use the following code to get started quickly.

```
DiscordClient client = new DiscordClient();
client.ClientPrivateInformation.Email = "email";
client.ClientPrivateInformation.Password = "pass";

client.Connected += (sender, e) =>
{
  Console.WriteLine($"Connected! User: {e.User.Username}");
};

client.SendLoginRequest();
Thread t = new Thread(client.Connect);
t.Start();
```