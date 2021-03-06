---
title: 'Quickstart: Recognize speech, C# (UWP) - Speech Service'
titleSuffix: Azure Cognitive Services
description: In this article, you create a C# Universal Windows Platform (UWP) application by using the Cognitive Services Speech SDK. You transcribe speech to text in real time from your device's microphone. The application is built with the Speech SDK NuGet Package and Microsoft Visual Studio 2017.
services: cognitive-services
author: lisaweixu
manager: nitinme
ms.service: cognitive-services
ms.subservice: speech-service
ms.topic: quickstart
ms.date: 07/23/2019
ms.author: lisaweixu
ms.custom: seodec18
---

# Quickstart: Recognize speech in a UWP app by using the Speech SDK

Quickstarts are also available for [text-to-speech](quickstart-text-to-speech-csharp-uwp.md), [speech-translation](quickstart-translate-speech-uwp.md) and [voice-first virtual assistant](quickstart-virtual-assistant-csharp-uwp.md).

If desired, choose a different programming language and/or environment:<br/>
[!INCLUDE [Selector](../../../includes/cognitive-services-speech-service-quickstart-selector.md)]

In this article, you develop a C# Universal Windows Platform (UWP; Windows version 1709 later) application by using the Cognitive Services [Speech SDK](speech-sdk.md). The program will transcribe speech to text in real time from your device's microphone. The application is built with the [Speech SDK NuGet Package](https://aka.ms/csspeech/nuget) and Microsoft Visual Studio 2017 (any edition).

> [!NOTE]
> The Universal Windows Platform lets you develop apps that run on any device that supports Windows 10, including PCs, Xbox, Surface Hub, and other devices.

## Prerequisites

This quickstart requires:

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/)
* An Azure subscription key for the Speech Service. [Get one for free](get-started.md).

## Create a Visual Studio project

[!INCLUDE [](../../../includes/cognitive-services-speech-service-quickstart-uwp-create-proj.md)]

## Add sample code

1. The application's user interface is defined by using XAML. Open `MainPage.xaml` in Solution Explorer. In the designer's XAML view, insert the following XAML snippet into the Grid tag (between `<Grid>` and `</Grid>`).

   [!code-xml[UI elements](~/samples-cognitive-services-speech-sdk/quickstart/csharp-uwp/helloworld/MainPage.xaml#StackPanel)]

1. Open the code-behind source file `MainPage.xaml.cs` (find it grouped under `MainPage.xaml`). Replace all the code in it with the following.

   [!code-csharp[Quickstart Code](~/samples-cognitive-services-speech-sdk/quickstart/csharp-uwp/helloworld/MainPage.xaml.cs#code)]

1. In the `SpeechRecognitionFromMicrophone_ButtonClicked` handler in this file, replace the string `YourSubscriptionKey` with your subscription key.

1. In the `SpeechRecognitionFromMicrophone_ButtonClicked` handler, replace the string `YourServiceRegion` with the [region](regions.md) associated with your subscription (for example, `westus` for the free trial subscription).

1. Save all changes to the project.

## Build and run the app

1. Build the application. From the menu bar, select **Build** > **Build Solution**. The code should compile without errors now.

    ![Screenshot of Visual Studio application, with Build Solution option highlighted](media/sdk/qs-csharp-uwp-08-build.png "Successful build")

1. Start the application. From the menu bar, select **Debug** > **Start Debugging**, or press **F5**.

    ![Screenshot of Visual Studio application, with Start Debugging option highlighted](media/sdk/qs-csharp-uwp-09-start-debugging.png "Start the app into debugging")

1. A window pops up. Select **Enable Microphone**, and acknowledge the permission request that pops up.

    ![Screenshot of permission request](media/sdk/qs-csharp-uwp-10-access-prompt.png "Start the app into debugging")

1. Select **Speech recognition with microphone input**, and speak an English phrase or sentence into your device's microphone. Your speech is transmitted to the Speech Services and transcribed to text, which appears in the window.

    ![Screenshot of speech recognition user interface](media/sdk/qs-csharp-uwp-11-ui-result.png)

## Next steps

> [!div class="nextstepaction"]
> [Explore C# samples on GitHub](https://aka.ms/csspeech/samples)

## See also

- [Translate speech](how-to-translate-speech-csharp.md)
- [Customize acoustic models](how-to-customize-acoustic-models.md)
- [Customize language models](how-to-customize-language-model.md)
