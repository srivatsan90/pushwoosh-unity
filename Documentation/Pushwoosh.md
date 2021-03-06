# class Pushwoosh #

Provides push notifications registration and handling and uniform access to the platform specific features.
Access it by calling `Pushwoosh.Instance` method.

```csharp
public class Pushwoosh : MonoBehaviour
```

Example:
```csharp
Pushwoosh.Instance.OnRegisteredForPushNotifications += onRegisteredForPushNotifications;
Pushwoosh.Instance.OnFailedToRegisteredForPushNotifications += onFailedToRegisteredForPushNotifications;
Pushwoosh.Instance.OnPushNotificationsReceived += onPushNotificationsReceived;
```

## Properties

### ApplicationCode

Set this variable to your Pushwoosh App Id.

```csharp
public static string ApplicationCode
```

---
### GcmProjectNumber

Set this variable to your Google Project Id For Android.

```csharp
public static string GcmProjectNumber
```

---
### HWID

Returns Device Unique Identifier.

```csharp
public virtual string HWID
```

---
### PushToken

Returns push notifications token. Could be empty if push notifications token has not been received yet.

```csharp
public virtual string PushToken
```

## Events

### OnRegisteredForPushNotifications

Push registration success delegate.

```csharp
public event RegistrationSuccessHandler OnRegisteredForPushNotifications = delegate {};
```

---
### OnFailedToRegisteredForPushNotifications

Push registration error delegate.

```csharp
public event RegistrationErrorHandler OnFailedToRegisteredForPushNotifications = delegate {};
```

---
### OnPushNotificationsReceived

Push notification handler delegate.

```csharp
public event NotificationHandler OnPushNotificationsReceived = delegate {};
```

## Methods

### RegisterForPushNotifications

Register for remote notifications

```csharp
public virtual void RegisterForPushNotifications()
```

---
### UnregisterForPushNotifications

Unregister from remote notifications

```csharp
public virtual void UnregisterForPushNotifications()
```

---
### SetIntTag

Sets Integer Tag for the device.

```csharp
public virtual void SetIntTag(string tagName, int tagValue)
```

---
### SetStringTag

Sets String Tag for the device.

```csharp
public virtual void SetStringTag(string tagName, string tagValue)
```

---
### SetListTag

Sets List Tag for the device.

```csharp
public virtual void SetListTag(string tagName, List<object> tagValues)
```

---
### StartTrackingGeoPushes

Starts tracking Geo Push notifications.

```csharp
public virtual void StartTrackingGeoPushes()
```

---
### StopTrackingGeoPushes

Stops tracking Geo Push notifications.

```csharp
public virtual void StartTrackingGeoPushes()
```

---
### ClearNotificationCenter

Clears all notifications from the system tray. iOS and Android only.

```csharp
public virtual void ClearNotificationCenter()
```

---
### SetBadgeNumber

Sets application icon badge number. iOS and Android only.

```csharp
public virtual void SetBadgeNumber(int number)
```

---
### AddBadgeNumber

Increments application icon badge number. iOS and Android only.

```csharp
public virtual void AddBadgeNumber(int deltaBadge)
```
