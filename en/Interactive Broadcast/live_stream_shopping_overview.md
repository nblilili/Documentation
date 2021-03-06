
---
title: Live-stream Shopping
description: 
platform: All Platforms
updatedAt: Fri Oct 16 2020 03:16:03 GMT+0800 (CST)
---
# Live-stream Shopping
## Introduction

Live-stream shopping combines e-commerce and live interactive video streaming. The host demonstrates their products in a live interactive streaming channel, and provides a product list with links; the audience can watch the host and place orders for desired products simply by clicking the links. During the interactive streaming, an audience member can become a co-host to interact with the host in real-time, asking for product details, negotiating prices, and sharing their experience of using the product. The host can also invite the host of another channel to co-host; the two hosts can then compete in promoting their products, thus stimulating the audience's enthusiasm for buying and enhancing the fun of live interactive streaming.

This article describes how to use the Agora SDKs to implement a live-stream shopping scenario.

## Feature list

You can use the Agora SDKs to implement the following features in your project:

| <span style="white-space:nowrap;">Feature&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</span> | Description |
| ---------------- | ---------------- |
| Real-time communication	      | With ultra low latency, the audience see and hear the host in real time. |
| Real-time messaging	| Both the host and the audience can chat with each other through text messages.|
| Interactive co-hosting       | The host invites an audience member or an audience member applies to become a co-host. All audience members in the channel can see and hear the host and co-host interacting with each other in real time. |
| Co-host across channels      | Hosts from two channels engage in online contests, and audiences from both channels watch the hosts. |
| Switching channels           | Audience members can switch between channels to buy desired products, send gifts, or cast votes to whichever host they like. |
| Managing product list        | The host manages the product list and provides links to the products. The audience can buy the products while watching the live interactive streaming. |
| User status	| Both the host and the audience are notified when a user joins or leaves the channel. |
| Real-time quality statistics	| Before joining a channel or during the live interactive streaming, all users can check the network quality in real time. |
| Background music |  For better interaction effects, the host can play background music when talking or singing. |
| Image enhancement	 | Basic image enhancement effects, including skin smoothening and cheek blushing, help the host look better. |

## Try the demo app

Agora provides the live-stream shopping demo apps on the following platforms:

| Android | iOS | 
| ---------------- | ---------------- |
| ![](https://web-cdn.agora.io/docs-files/1594967764588)     | ![](https://web-cdn.agora.io/docs-files/1594287505817)      | 

Since a live-stream shopping scenario has multiple users, Agora recommends downloading and installing the demo app on **two** mobile devices. After installation, follow these steps to test the demo app:

1. On one device, click **Agora Live**, and choose **Live Stream Shopping**.
2. Click the **Camera** icon on the lower right, and then enter a room name to create a channel. Click **Start** to start the live interactive streaming as a host.
3. On the other device, click **Agora Live**, choose **Live Stream Shopping**, and join the created channel to watch the interactive streaming as an audience member.
4. On the host side, tap the ![](https://web-cdn.agora.io/docs-files/1602226164257) icon at the bottom of the screen to expand the product list. Choose the products in the **Pending** column and click **Launch** to put the chosen products on sale.
5. On the audience side, click the product list to see the products for sale. Select the product that you want to buy and click its link to place an order. 
6. During live-stream shopping, the host can click the **PK** icon to invite the host of another channel to begin co-hosting; an audience member can become a co-host to interact with the host in real-time.

<div class="alert note">During the test, the demo app prompts to request authorization for the camera and audio recording. Grant permissions accordingly.</div>

## Technical solutions

The live-stream shopping scenario involves two basic scenarios:
- Real-time engagement in a channel
- PK host across channels

The technical architecture for each scenario is as follows:

**Real-time engagement in a channel**
![](https://web-cdn.agora.io/docs-files/1602226332063)

**PK host across channels**
![](https://web-cdn.agora.io/docs-files/1602226361077)

| Product | Function |
| ---------------- | ---------------- |
| Agora RTC SDK      | Joins an RTC channel for real-time audio and video communication.      |
| Agora RTM SDK | Logs into the RTM system and joins an RTM channel for sending and receiving text messages. |
| Third-party Image Enhancement SDK | Sets basic image enhancement effects, including skin smoothening and cheek blushing. |


## Advantages

**Ultra low latency** 

Agora SD-RTN<sup>TM</sup> is the Agora proprietary network for audio and video transmission, covering more than 200 countries and regions. It uses the intelligent routing algorithms to ensure that the average end-to-end latency worldwide is less than 400 ms.

**Stability and reliability**

The Agora SLA (Service Level Agreement) ensures a 99%+ login success rate and 99.99% service accessibility throughout the year.

**Excellent performance under poor network conditions**

With an industry-leading algorithm designed to minimize the impact of packet loss, Agora guarantees smooth audio and video communication when the packet loss rate reaches 70%, and smooth audio communication when the packet loss rate is as high as 80%.

When a user's network bandwidth is poor, our self-adaptive strategy prioritizes the communication of the audio and the host.

**High audio quality**

The following technologies ensure that the speaker's voice always stands out from a noisy environment:

- A maximum audio sampling rate of 48 kHz for full band frequency.
- The 3A algorithm featuring automatic echo cancellation (AEC), automatic noise suppression (ANS), and automatic gain control (AGC).

**Voice changer**

During live interactive streaming, adding voice changer and reverberation effects brings much fun and enhances the atmosphere of the live room. Agora provides an enriched selection of voice changer options, which developers can easily implement by calling an API.

**High-definition video**

Agora optimizes the video experience from the following perspectives:

- Supports a maximum resolution of 4K to accommodate the growing demand for high-definition video.
- Works with most main-stream devices, platforms, and scenarios by supporting H.265 codec, super resolution, and perceptual video coding.
- Uses a dynamic bitrate algorithm to adapt the video bitrate to the real-time network conditions for resolutions from 48p to 1080p.
- For a set resolution and frame rate, consumes less bandwidth and renders higher quality video.

**Support for third-party services**

For more enriched and diversified scenarios, you can easily import third-party services into your project, such as content moderation, image enhancement, and AR.

**Traceability**

- Agora provides a variety of methods for measuring network quality. We also have callbacks that report on communication quality during live interactive streaming. Use these methods to ensure a smooth experience and to troubleshoot quality issues.
- You can also use [Agora Analytics](https://console.agora.io/analytics/call/search) to monitor the quality, user behavior, device state, and Quality of Experience (QoE)/Quality of Service (QoS) statistics.

**Compatibility**

Agora SDKs are compatible with more than 6,000 devices, covering over 18 platforms and development architectures, including Windows, macOS, Web, iOS, Android, and Electron. This ensures that all users share the same experience.
