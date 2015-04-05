accounts-sms
=============
Allow users to login with their phone number. **WIP -- use at your own risk.**

##Usage

`meteor add dispatch:accounts-sms`

**Server**

```
// Configure to use twilio.
Accounts.sms.configure({
  twilio: {
    from: Meteor.settings.TWILIO.FROM,
    sid: Meteor.settings.TWILIO.SID,
    token: Meteor.settings.TWILIO.TOKEN
  }
});
```

**Client**

```
// Send the verification code sms.
Meteor.sendVerificationCode('+12222222222');
```

```
// Login with the verification code sms.
Meteor.loginWithSms('+12222222222', '2222');
```

```
// Lookup a phone number
Meteor.lookup('+12222222222');
```
