---
title: "Testing iOS In-App Purchases with Sandbox"
description: "A beginner's guide to setting up sandbox testing for your iOS app"
---

# iOS Sandbox Testing Guide

## What Is Sandbox Testing?

Sandbox testing lets you test in-app purchases without using real money. It's an essential step before launching your app.

## Create a Sandbox Account

1. Go to [App Store Connect](https://appstoreconnect.apple.com/)
2. Navigate to **Users and Access > Sandbox Testers**
3. Click the **+** button
4. Enter your email address (must be verifiable) You could for instance just use your email with "sandbox" in it (e.g. "steffen+sandbox@buildwithai.io")
5. Fill in the required fields and select a region
6. Click **Save**

## Testing on Your Device

### Step 1: Install Your App

Install your development build on your iOS device.

### Step 2: Make a Purchase

When you try to make a purchase, you'll be prompted to sign in with your sandbox account credentials.

> **Note:** After your first purchase, iOS will remember your sandbox account.

### Step 3: Add Sandbox Account to Settings (Optional)

For easier testing, add your sandbox account to settings:

- iOS 13-17: **Settings > App Store > Sandbox Account**
- iOS 18+: **Settings > Developer > Sandbox Apple Account**

If you don't see these options, make a sandbox purchase first.

## Important Things to Know

### Subscription Testing

Subscription renewals are accelerated in sandbox mode:

| Real Subscription | Sandbox Renewal |
|-------------------|----------------|
| 1 month           | 5 minutes      |
| 1 year            | 1 hour         |

### Common Issues

- **Slow response:** Sandbox purchases may take up to 15 seconds. This is normal.
- **Price differences:** Prices may not match what you set in App Store Connect. Focus on testing the purchase flow, not the exact prices.

### Verifying Purchases

After a purchase, check your RevenueCat dashboard with the "View Sandbox Data" toggle enabled.

## Reset Your Testing Environment

### To test as a new user:

1. Uninstall and reinstall your app
2. Create a new sandbox account if needed

## TestFlight Testing

In TestFlight, all subscription renewals happen once per day regardless of the original duration.

## Need More Help?

See [Apple's official documentation](https://developer.apple.com/documentation/storekit/in-app_purchase/testing_at_all_stages_of_development_with_xcode_and_the_sandbox) for advanced topics.