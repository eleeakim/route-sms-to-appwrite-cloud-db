# SMS Broadcast Receiver for Android with Appwrite Integration

This repository contains a simple Android broadcast receiver implementation that listens for incoming SMS messages and integrates with Appwrite for database storage.

## Introduction

Broadcast receivers are components that enable your app to listen for system-wide events or intents. In this case, we are specifically interested in capturing incoming SMS messages. 

Additionally, Appwrite is an open-source platform that provides a set of tools and services for building web and mobile applications. 

## Implementation Details

The `SmsBroadcastReceiver` class extends the `BroadcastReceiver` class provided by Android. Inside the `onReceive()` method, we check if the received broadcast is for SMS messages. If it is, we extract the sender's number and the message content from the intent and pass them to the `main()` function.

The `main()` function initializes an Appwrite client with the provided project details and creates a document in the specified database and collection. The document contains fields for the sender's number and the message content.

## Prerequisites

- Android development environment set up.
- Appwrite project created with database set up.

## Usage

To use this broadcast receiver in your Android project:

1. Copy the `SmsBroadcastReceiver` class into your project.
2. Make sure to replace `<PROJECT_ID>`, `<DATABASE_ID>`, and `<COLLECTION_ID>` with your actual project details.
3. Register the broadcast receiver in your AndroidManifest.xml file with the appropriate permissions.

## License

This project is licensed under the MIT License.

## Acknowledgments

- This project was inspired by the need to integrate SMS functionality with Appwrite.
- Special thanks to the contributors of the Appwrite platform for providing a robust set of tools for app development.


