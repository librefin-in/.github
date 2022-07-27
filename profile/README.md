Welcome to librefin.in, a community project to get us to a Free and Open Source UPI implementation.

## Approaches

There are broadly 2 approaches to interact with UPI an in interoperable manner (ie, not getting limited to just customers from one bank):

1. Using `*99#` as the base-minimum feature-set, and wrap it in applications.
2. Reverse-engineer, document and clean-room reimplement the various codebases used by other UPI applications.

There are pros and cons to both approaches - notable:

1. USSD programmability is quite limited: Only for certain prompts, and only on certain mobile devices (Android 8.0+).
2. `*99#` is not supported on all telecom carriers, and especially doesn't work outside of India.
3. Reversing and re-implementing applications is a lot of hard work. However, many applications are outsourced to vendors and are re-skinned variants with different endpoints, making the job easier.
4. We only need one complete backend re-imeplementation to get a complete app.
5. Attempting full programmability for USSD codes requires Accessibility permissions on Android.
6. There's a lot of prior art and FOSS tech tailor made for wrapping USSD codes in Android applications.

## Current Status:

- [x] Document the common library specification: https://github.com/librefin-in/cl-specification
- [x] Reimplement the common library from the specification: https://github.com/librefin-in/cl
- [x] Document the `*99#` schema: https://github.com/librefin-in/nuup-specification
- [x] Document the bank API schema for atleast one bank: https://github.com/librefin-in/openapi-cointab
- [ ] Launch a minimal `*99#` wrapper application.

## How to contribute

1. We're looking for mobile developers, or platform developers willing to own a UPI implementation for a specific platform.
2. Reverse-engineers looking to help documenting APIs are also welcome - the bar to entry is lower than you think.
3. An Android application that wraps the NUUP schema using accessibility APIs will be a great first launch, even if with minimal features.

You can also join us on Gitter: https://gitter.im/librefin-in/community, or on Telegram: https://t.me/librefin

## Questions?

Please file an issue in this repository for general questions, or in the other repositories for specific questions. You might wanna follow @captn3m0 on Twitter for announcements - look out for a townhall soon.
