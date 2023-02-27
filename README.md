# VNPAY Wallet

VNPAY Wallet is a PHP library that provides payment gateway integration for websites. It allows users to make payments using their VNPAY accounts. It is designed to be easy to use and highly customizable, so you can integrate it seamlessly into your website.

## Features

Here are some of the key features of VNPAY Wallet:

- Easy integration: You can integrate VNPAY Wallet into your website with just a few lines of PHP code.
- Customizable: You can customize the look and feel of the payment form to match your website's design.
- Secure: VNPAY Wallet uses industry-standard encryption and security protocols to keep your users' data safe.
- Fast: Payments are processed quickly, so your users won't have to wait long to complete their transactions.

## Getting Started

To use VNPAY Wallet on your website, you will need to follow these steps:

1. Create a VNPAY account if you don't already have one.
2. Download the latest version of VNPAY Wallet from the releases page on GitHub.
3. Extract the contents of the ZIP file to a directory on your web server.
4. Include the following files in your PHP page:
    - `VnPay.php`
    - `VnPayConfig.php`
5. Initialize VNPAY Wallet by creating a new instance of the `VnPay` class and setting the appropriate configuration options.

## Usage

To use VNPAY Wallet on your website, you will need to create a payment form that collects the necessary information from the user. Here's an example of the data you need to collect:

- `vnp_Amount`: The amount of the payment in Vietnamese dong (VND).
- `vnp_OrderInfo`: A brief description of the payment.
- `vnp_TxnRef`: A unique identifier for the payment.
- `vnp_ReturnUrl`: The URL to redirect the user to after the payment is complete.
- `vnp_IpAddr`: The IP address of the user making the payment.

Once you have collected this information, you can create a new instance of the `VnPay` class and call the `buildCheckoutUrl()` method to generate a URL for the payment form. You can then redirect the user to this URL to initiate the payment process.

## Contributing

Contributions to VNPAY Wallet are always welcome! Here are some guidelines to follow when contributing:

- Submit bug reports and feature requests on the GitHub Issues page.
- Follow the coding conventions and style guidelines in the CONTRIBUTING.md file.
- Submit pull requests to the master branch.

## License

VNPAY Wallet is released under the MIT License. See the LICENSE file for more information.

## Additional Notes

- This is a fork of the original repository, which has been archived and is no longer maintained.
- The original repository can be found here: https://github.com/vnpay/vnpay-wallet.
