---
title: Enhance chat transcript security with IP whitelisting
sidebar_label : Chat transcript security
---
Chat transcripts are vital records of interactions between users and chatbots, whether they are [conversation logs](https://docs.yellow.ai/docs/platform_concepts/studio/analyze/chat-logs) or [chats with agents](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/workflows/chattranscript). To ensure top-notch security, our platform has introduced a cutting-edge feature that allows access to these conversations exclusively from specified whitelisted IP addresses.
This feature is available on the app and cloud platform. 

-----

## IP whitelisting workflow

### Enable chat transcript security

When the chat transcript security feature is enabled for a bot, users must meet at least one of the following criteria:
- **Users with Bot Access**: If the user already has access to the bot, they can seamlessly view the chat transcript links without the need to whitelist their IP address. However, users must have an active session (logged into the platform) to access the chat transcript links. If not logged in, they will be prompted to log in before viewing the links.
- **Users without Bot Access**: Users who do not have access to the bot can access the chat transcript links only by whitelisting their IP address.

**![](https://lh3.googleusercontent.com/6KbmFZCKa3IuRp51mHyjW2T_Ep2ndBM78NjK0U-QbhRLtOllyskOZC3pMSvDN05EsyrkNCVw1eQfjFJZBKfTbROrXv1uwfvNjQU6QCI8S2Hxio2snL_5bBYWlwJcQHuhzP6HoEoOzKlf7ZeLQSsucP0)**

### Access chat transcript links

For users without bot access and without whitelisted IP addresses, the chat transcript link will appear as follows:

![](https://lh5.googleusercontent.com/XH9QRh16jYSPzPunTglnjRKGqbxkD3DK5iSDYIFOc515n6tjcScKdLlRjuWEOdQHC8TdPcJuYj1sW1YQbJZP_9FJXrwsB1zqjs7-NDpzKwoUhOItyrSMeEU7tzFN3DQH8tKxtgso7bJeOqyNjcKjZqU)

------

## Enable IP whitelisting on the app platform


To access the Security Settings feature on the app platform, follow these simple steps:

1. Navigate to the **Configuration** tab for your bot on the platform.
2. Click on the **Security** tab located at the top of the page.

**![](https://lh3.googleusercontent.com/9YDa7L8_bAYG6gV0qUhk6c9c1WQukW1Ijr3OA5Yl9Zxm06_ghYeaAgZMDXLy-SN-uy0dpC5CE8x6zrBaoOgWkE1_GLB1ReHSN_n-dpF7vnc_4AHoXOm4IEeln3t81Vmsq2RWsoQ4uNB3yhJAIo3i6OU)**

**Steps to enable IP whitelisting for a specific bot on the app platform**

1. Enable the **IP Whitelisting** feature by clicking the toggle button.
**![](https://lh4.googleusercontent.com/9MP2TNgB2vh36HWlhrdUKKMZa2BZcIV1GF5lhsoESB8Hxuh9B7UqjegKhiSGjXa9OEEZyoZukvI2oxrpd1NjAEETFhgjfwEKf1m_7eG-bRnLBUAgHahBE1my9VyXy10L8cRFQwI22lsev-2NkrP7FLs)**

2. To add IP addresses, click on the **Add IP Range** button.
**![](https://lh5.googleusercontent.com/4hf7_bb-Nt7eoY5_zSHF64JyCXmK_VGNG6I6H-3whjrXkS8tgP7ycFF_yAvuhFfAYBb92qWb0K6SEdiq3arPu1rd5oUWttpTFvbtwbPzs2mstILK3BE-j8zx-lEQyYYDD8KBWMrf0hX4Rmudj7tbpjg)**

3. After adding the IP range, it will be displayed on the dashboard.
**![](https://lh6.googleusercontent.com/oEkxbpjkai3lVHnu00neRQGVowdXovE8ENIOR5P_EqkQnezCtiQpNfpDUAoc0GBRjRImBl6tA30UEADJTYr6PRK603Kcc0tqe-tQx5anJYIkdwmNt4n_yLmgR4mb_BmuYZpws1vLmGcpSzp3q7ZYOnA)**

:::note
- Only IPV4 addresses are currently supported.
- If you wish to whitelist only one IP address, simply add the same IP address in both the **Start IP Range** and **End IP Range** fields.
:::

-------

## Enable IP whitelisting on the cloud platform

To access the Security Settings feature on the Cloud Platform, follow these steps:

1. Navigate to the Studio module for your bot on the platform.
**![](https://lh5.googleusercontent.com/M0Cg36WbmlozBBsin6gMCODBR8J3r4ymBR4UQRn5icQt8BkYgtG7_WL4Zjf9ME-iQ7IKNmNwFg1HaR-U7GNXdbNC_h-Vd9uGauajd7ypBX2aQtf-K20NWoYVDONMb3MCjXaiY37rRm3O4UIPEUg6Qb8)**
2. Click on the Access Control tab located at the top of the page.
3. Enable the IP Whitelisting feature by clicking the toggle button.
**![](https://lh6.googleusercontent.com/fesPMUsYERq3UOvyGgzYTgo5ufhkIdBQ1TjPc7ZEKjVfVHkZar46yJ6jccc5p6gJe8MKuaJ2AdnPl6fBU9k7AQIOO9R1jVBWa0a-Ck5vZY9yuTMHtzY9yxjQEnnK-42wtua6vPUoXzMho0FG3DG9Gd0)**

**Steps to enable IP whitelisting for a specific bot on the cloud platform**

1. Click on the toggle button, which will reveal an option to add IP addresses, as shown in the screenshot below.
**![](https://lh4.googleusercontent.com/drnS-oPdet6kkIxln8fxLYyVgU-IPYpHn3BaoWvNl0opmcZWuvrol3bR_V20f_FQ1X3OzK8oM-V_129gppP_iqgxyRZ5qi281PMO7yPi4AS-EEcHhOotoJEOK5Mzo_YRhdqX-K8VGAne3qe2sh6zFkE)**
2. Click on the **Add IP Range** button to include the IP address range from which chat transcripts can be accessed.
**![](https://lh6.googleusercontent.com/2UEIfqbFn0xNjkwlOhbMrfJ8R4o2Rv9womsufhMPKLp2SyZZUTB-GjwPoWZtiRwl47gDeO12AM21Hm5w0dXo1zrrcrRWXnqQnxgrPAISavGheVoBkTkQSi7Fwu_7HJiRjbe_nrNgycneu6Ro5vcK3ro)**
3. After adding the IP range, it will be displayed on the dashboard.
**![](https://lh3.googleusercontent.com/Qp4kSiGvSG3_c3Yn1Vq1hhXIVuwvh5EmVxTp0mBwqtYWpFGzSJe6c8kA3umm5wUy27aBR437JYL9i56MZob2tCtiRxiohNKfQgiLzjVc2LwvieW8Hjxu-U5Xo3FXnhBvUzRf8XjbJ6b9Ve05sr74hEA)**

:::note
- Only IPV4 addresses are currently supported.
- If you wish to whitelist only one IP address, simply add the same IP address in both the **Start IP Range** and **End IP Range** fields.
:::