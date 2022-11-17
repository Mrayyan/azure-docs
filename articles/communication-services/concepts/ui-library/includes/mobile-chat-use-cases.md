Use the chat composite in the Azure Communication Services UI Library to create chat experiences in your for iOS and Android applications. By using a couple lines of code, you can easily integrate an entire chat experience in your application. Composites in Communication Services manage the entire lifecycle of the chat, from setup until the chat ends.

## Chat use cases

| Area         | Use cases                                        |
| ------------ | ------------------------------------------------ |
| Chat types   | Join a Microsoft Teams meeting chat                        |
|              | Join an Azure Communication Services chat thread |
| Chat actions | Send a chat message                                |
|              | Receive a chat message                             |
| Chat events  | Show typing indicators                                |                                     |
|              | Show when a participant is added or removed                        |
|              | Show changes to the chat title                               |
| Participants | Show a participant roster                               |

## Supported identities

To initialize a composite and authenticate to the service, a user must have an Azure Communication Services identity. For more information, see [Authenticate to Azure Communication Services](../../authentication.md) and [Quickstart: Create and manage access tokens](../../../quickstarts/access-tokens.md).

## Teams interoperability

For [Teams interoperability](../../teams-interop.md) scenarios, you can use UI Library composites to add a user to a Teams meeting chat via Communication Services. To enable Teams interoperability, use the Chat composite. The composite manages the entire lifecycle of joining a Teams interoperability Chat.


## Theming

You can use the UI Library Chat composite for iOS and Android to create a custom theme of a Chater's experience. To create the platform experience, pass a set of theming colors as shown in the following table. For more information, see [How to create your theme](../../../how-tos/ui-library-sdk/theming.md).


## Screen size

You can adapt the Azure Communication Services Chat composite to adapt to screen sizes from 5 inches to tablet size. Use split mode and tablet mode in the Chat composite to get the dynamic participants' roster layout, provide clarity on the view, and focus on the conversation.


## Localization

Localization is key to making products for users around the world and who speak different languages. UI Library supports 12 languages: English, Spanish, French, German, Italian, Japanese, Korean, Dutch, Portuguese, Russian, Turkish, and Chinese. It also supports right-to-left languages. For more information, see [How to add localization to your app](../../../how-tos/ui-library-sdk/localization.md).

## Accessibility

Accessibility is a key focus of the Chat libraries. You can use a screen reader to make important announcements about Chat status and to help ensure that visually impaired users can effectively participate when they use the application.

## Recommended architecture

Initialize a composite by using an Azure Communication Services access token. It's important to get access tokens from Azure Communication Services through a trusted service that you manage. For more information, see [Quickstart: Create and manage access tokens](../../../quickstarts/access-tokens.md) and the [trusted service tutorial](../../../tutorials/trusted-service-tutorial.md).

:::image type="content" source="../../media/mobile-ui/ui-library-architecture.png" border="false" alt-text="Diagram that shows the recommended architecture for UI Library.":::

Call and chat client libraries must have the context for the Chat they join. Like user access tokens, disseminate the context to clients by using your own trusted service. The following table summarizes the initialization and resource management functions that are required to add context to a client library:

| Contoso responsibilities                                 | UI Library responsibilities                                     |
| -------------------------------------------------------- | --------------------------------------------------------------- |
| Provide an access token from Azure                          | Pass through the provided access token to initialize components       |
| Provide a refresh function                                 | Refresh the access token by using a developer-provided function          |
| Retrieve and pass join information for the Chat or call          | Pass through Chat and chat information to initialize components |        |

## Platform support

|Platform | Versions|
|---------|---------|
| iOS     | iOS 14 and later |
| Android | API 23 and later |

> [!div class="nextstepaction"]
> [Quickstart guides](../../../quickstarts/ui-library/get-started-composites.md)
