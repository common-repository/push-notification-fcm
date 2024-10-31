=== Push Notification FCM ===
Contributors: ivijanstefan, creativform
Tags: Firebase Cloud Messaging, FCM, push notifications, Android, iOS, integration, REST API, device registration
Requires at least: 5.0
Tested up to: 6.4
Requires PHP: 7.0
Stable tag: 1.0.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Donate link: https://www.buymeacoffee.com/ivijanstefan

Introducing a seamless framework plugin for Firebase Cloud Messaging (FCM) for Android and iOS developers, to send push notifications globally.

== Description ==

This FCM Plugin for WordPress is designed to simplify the integration of push notifications to all Android and iOS devices. With ease of use in mind, here's what you can achieve:

1. **Easy Integration**:
   - **Installation**: Simply install the plugin.
   - **Configuration**: Enter your Firebase Server (API) key, generate a site key, and select the post types for notifications.
   - **Compatibility**: Works with both Android and iOS devices and the latest version of WordPress.

2. **REST API Endpoints for Device Management**:
   - **Subscribe Device**: Register devices when the mobile application is launched.
   - **Unsubscribe Device**: Deregister devices when the application is deleted.
   - **Example**: Use the provided endpoints with parameters like `rest_api_key`, `device_uuid`, `device_token`, etc., to manage subscriptions.

3. **Customizable Notifications**:
   - **Categories**: Register devices under specific categories. If a category doesn't exist, it'll be created automatically.
   - **Content Types**: Select specific post types for triggering notifications.

4. **Open Source & Free**: Modify and use without any cost.

Make sure to have a Firebase project and your Firebase Server (API) key before using the plugin. Don't miss out on important updates, try our FCM push notification plugin today!

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/` directory, or install through the WordPress plugins screen.
2. Activate the plugin.
3. Enter your Firebase Server (API) key and generate a site key in the plugin settings page.
4. Select the types of posts for notifications.

== REST API Endpoints ==

### Subscribe Device
`https://example.domain/wp-json/fcm/pn/subscribe`
Parameters:
- `rest_api_key` (required): Unique site key from plugin settings.
- `device_uuid` (required): Device's unique ID.
- `device_token` (required): Device's token.
- `subscription` (required): Category name for device registration.
- `device_name` (optional): Name of the device.
- `os_version` (optional): Operating system version.

Returns JSON:
`
{
	"error": false,
	"message": "Device token registered",
	"subscription_id": 123
}
`

**Unsubscribe device:**

`https://example.domain/wp-json/fcm/pn/unsubscribe`

**Parameters:**

* `rest_api_key` (required): Unique site key from plugin settings.
* `device_uuid` (required): Device's unique ID.

**Returns JSON:**
`
{
	"error": false,
	"message": "The device token was successfully removed"
}
`

This plugin is available as open-source and free of charge, allowing seamless integration with any WordPress setup and offering the flexibility for customization to meet specific needs.

== Screenshots ==

1. General plugin settings
2. All registered devices
3. Settings within the article for push notifications
4. WP-JSON REST API format for Subscribe
5. WP-JSON REST API format for Unsubscribe
6. Test and Compatibility

== Changelog ==

= 1.0.0 =
* First stabile version

= 1.0.1 =
* Improved REST API
* Improved UX
* Improved documentation

= 1.0.2 =
* Improved plugin security
* Improved plugin cache

= 1.0.3 =
* Added support for the WordPress version 6.3.x

= 1.0.6 =
* Bugfixes

== Upgrade Notice ==

= 1.0.6 =
* Bugfixes

== Other Notes ==

1. **Preparation for Use**:
   - Prior to activating the plugin, it's essential to establish a Firebase project and obtain the corresponding Firebase Server (API) key. This setup links your WordPress site to Firebase, enabling the key functionalities of the plugin.

2. **Unique Site Key Requirement**:
   - Upon installing the plugin, you'll need to access the plugin settings page to generate a unique site key. This key is crucial for the identification and security of your particular WordPress installation.

3. **Content-Type Selection for Notifications**:
   - The plugin grants you the flexibility to choose specific types of posts for sending notifications. This allows for a tailored communication strategy, ensuring that users only receive alerts relevant to their interests.

4. **Device Management via REST API Endpoints**:
   - The plugin utilizes REST API endpoints to manage device registration and deregistration. Your mobile application must be configured to interact with these endpoints, enabling accurate control over the device subscriptions.

5. **Cross-Platform Compatibility**:
   - Designed to work seamlessly with both Android and iOS devices, this plugin ensures that you can reach your audience regardless of their preferred platform.

6. **Category-Specific Notification Delivery**:
   - The plugin facilitates sending push notifications to all registered devices for a particular post category. This targeted approach enhances engagement by delivering content-specific alerts.

7. **Registration Verification Before Notification**:
   - Prior to sending any notifications, the plugin verifies the device's registration status. This step maintains notification accuracy and avoids sending to inactive or irrelevant devices.

8. **Compatibility with Latest WordPress Version**:
   - While the plugin aligns with the most recent WordPress version, it's advisable to check for compatibility to ensure a smooth integration within your specific WordPress environment.

9. **Customizable Open-Source Software**:
   - Embracing an open-source model, the plugin's code can be adapted to meet individual requirements. This encourages not only personalized use but also potential community contributions and collaboration.

== Installation ==

To install the "Push Notification FCM" plugin via the WordPress admin dashboard, follow these steps to enable push notifications for your website:

1. **Log In**: Access your WordPress site with administrator credentials.
2. **Navigate to Plugins**: Locate the "Plugins" section within your WordPress dashboard.
3. **Add New Plugin**: Click on the "Add New" button to explore new plugins.
4. **Search for the Plugin**: Enter "Push Notification FCM" in the search bar to find the specific plugin.
5. **Install the Plugin**: Click on the "Install" button adjacent to the plugin and wait for the installation to complete.
6. **Activate the Plugin**: Click on the "Activate" button to enable the plugin's functionalities.
7. **Configure Settings**: Navigate to the "Push Notification FCM" settings page to enter your Firebase Server (API) keys, generate a site key, and select the types of posts for push notifications.
8. **Integrate with Mobile App**: Insert the generated REST endpoints of your site into your mobile application to facilitate device registration.
9. **Start Push Notifications**: With everything in place, you can now commence sending push notifications to all subscribed devices.

**Note**: Prior to installation, please ensure that the plugin is compatible with your specific version of WordPress. Compatibility information is vital for smooth integration and optimal performance.

== Frequently Asked Questions ==

= What is the "Push Notification FCM" plugin? =

The "Push Notification FCM" plugin is a free and open-source tool designed for WordPress, enabling website owners to send push notifications to Android and iOS devices worldwide. Utilizing Firebase Cloud Messaging (FCM), it simplifies integration, allowing administrators to select specific post types for notifications, and manage device registration and deregistration via REST API endpoints. The plugin ensures compatibility with both Android and iOS, and its open-source nature allows for customization as per individual requirements. It offers a seamless way to keep users informed about new articles or updates and can be installed and configured directly from the WordPress dashboard.

= How do I install the plugin? =

Installing the "Push Notification FCM" plugin is a straightforward process, and it can be done in one of two ways:

1. **From WordPress Plugin Repository**: Download the plugin directly from the WordPress plugin repository.

2. **Upload Via Dashboard**: Alternatively, you can upload it to your WordPress site via the "Plugins" section within the WordPress dashboard.

**Configuration Steps**:

1. **Activate the Plugin**: Once installed, activate the plugin to enable its functionalities.
2. **Enter Firebase Server (API) Key**: Provide your specific Firebase Server key to establish the connection.
3. **Generate Site Key**: Create a unique site key tailored to your WordPress installation.
4. **Select Notification Types**: Choose the particular types of posts for which you wish to send notifications.

With these steps completed, your site is now equipped to send push notifications via the "Push Notification FCM" plugin.

= What are the REST API endpoints provided by the plugin? =

The "Push Notification FCM" plugin provides two REST API endpoints:

1. **Subscribe Device Endpoint**: Used to register a device with the site to receive notifications, requiring details like the site key, device ID, and token.
2. **Unsubscribe Device Endpoint**: Used to deregister a device from receiving notifications, requiring the site key and device ID.

These endpoints facilitate the management of device subscriptions for receiving push notifications.

= Is this plugin free to use? =

Yes, the plugin is a free and open-source software, which means that it can be used in any WordPress installation without any cost and can be modified as per the requirement.

= How do I subscribe or unsubscribe devices for push notifications? =

You can subscribe or unsubscribe devices for push notifications using the REST API endpoints provided by the plugin. The endpoints require specific parameters, such as the device's unique identification (ID) and token, as well as a unique generated site key provided by the plugin.