# Bunker Marketplace - Installation Guide

This installation guide will walk you through the process of setting up the Bunker Marketplace on your server. Please follow the steps below:

## Prerequisites

Before starting the installation, make sure you have the following:

- Ubuntu 22 server
- Apache webserver
- PHP 8
- MySQL database
- Monero wallet RPC running on localhost:18080

## Step 1: Clone the Repository

1. Open a terminal on your server.
2. Navigate to the `/var/www/html/` directory: `cd /var/www/html/`.
3. Clone the repository: `git clone https://github.com/your-repo-url.git`.
4. Change the ownership of the cloned files to the web server user: `chown -R www-data:www-data /var/www/html/`.

## Step 2: Configure the Database

1. Create a new MySQL database for the marketplace.
2. Import the database schema from the `database.sql` file provided in the repository.

## Step 3: Configure the Marketplace

1. Rename the `config.example.php` file to `config.php`.
2. Open the `config.php` file and update the following variables:
   - `DB_HOST`: The hostname of your MySQL database server.
   - `DB_USERNAME`: The username to access your MySQL database.
   - `DB_PASSWORD`: The password to access your MySQL database.
   - `DB_NAME`: The name of the MySQL database for the marketplace.
   - `MONERO_RPC_HOST`: The hostname of your Monero wallet RPC server.
   - `MONERO_RPC_PORT`: The port number of your Monero wallet RPC server.
   - `MONERO_RPC_USERNAME`: The username to access your Monero wallet RPC server.
   - `MONERO_RPC_PASSWORD`: The password to access your Monero wallet RPC server.
   - `COINGECKO_API_URL`: The URL of the CoinGecko API.
   - `COINGECKO_API_ENDPOINT`: The endpoint of the CoinGecko API for USD conversion.
   - `COINGECKO_API_CURRENCY`: The currency to use for USD conversion.
3. Save the `config.php` file.

## Step 4: Configure the Admin Dashboard

1. Rename the `admin/config.example.php` file to `admin/config.php`.
2. Open the `admin/config.php` file and update the following variables:
   - `APP_NAME`: The name of the marketplace (default: Bunker).
   - `ADMIN_USERNAME`: The username for the admin dashboard (default: mrbunker).
   - `ADMIN_PASSWORD`: The password for the admin dashboard (default: 12345678).
3. Save the `admin/config.php` file.

## Step 5: Set Permissions

1. Set the correct permissions for the `uploads` directory: `chmod -R 777 uploads`.

## Step 6: Access the Marketplace

1. Open a web browser and enter your server's domain or IP address.
2. You should see the Bunker Marketplace homepage.
3. To access the admin dashboard, go to `domain.tld/admin` and enter the admin username and password configured in Step 4.

## Step 7: Adding New Categories

1. Log in to the admin dashboard.
2. Navigate to the "Categories" section.
3. Click on the "Add New Category" button.
4. Enter the name of the new category and click "Save".

Congratulations! You have successfully installed and configured the Bunker Marketplace. You can now start using it to buy and sell products.

If you have any further questions or need assistance, please don't hesitate to contact our support team.