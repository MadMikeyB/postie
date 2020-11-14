# UPS

### How to get API access

Register for an access key via the [UPS Developer Kit](https://www.ups.com/upsdeveloperkit?loc=en_US) form. Add this access key in the provider information either through the control panel, or in the configuration file (as the API Key).

### Services

The below service are available with UPS for domestic and international customer destination addresses.

- `S_AIR_1DAYEARLYAM`
- `S_AIR_1DAY`
- `S_AIR_1DAYSAVER`
- `S_AIR_2DAYAM`
- `S_AIR_2DAY`
- `S_3DAYSELECT`
- `S_GROUND`
- `S_SURE_POST`
- `S_STANDARD`
- `S_WW_EXPRESS`
- `S_WW_EXPRESSPLUS`
- `S_WW_EXPEDITED`
- `S_SAVER`
- `S_ACCESS_POINT`

### Configuration

Add the following code to your configuration file under the `providers` array, as per the below. Note that to disable certain services, simply omit them from the `services` array.

```php
'providers' => [
    'ups' => [
        'name' => 'USPS',

        'settings' => [
            'apiKey' => 'xxxxxxxxxxxxxxxxxxxxx',
            'testApiKey' => 'xxxxxxxxxxxxxxxxxxxxx',
            'username' => 'xxxxxxxxxxxxx',
            'password' => 'xxxxxxxxxxxxx$',
        ],

        'services' => [
            'S_AIR_1DAYEARLYAM' => 'UPS Next Day Air Early AM',
            'S_AIR_1DAY' => 'UPS Next Day Air',
            'S_GROUND' => 'UPS Ground',
            'S_STANDARD' => 'UPS Standard',
        ],
    ],
]
```