# Installing Ruby on ARM64 using RVM

## Prerequisites

- Confirm OpenSSL 1.1.x is enabled:
  ```bash
  openssl version
  ```

  You should have OpenSSL 1.1.x. If it shows a different version, install OpenSSL 1.1.x first.

- **Install Homebrew:**
  If Homebrew is not installed, you can install it using the following command:
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
  ```

## Installation Steps

1. Install OpenSSL 1.1.x:
   ```bash
   brew install openssl@1.1
   ```

2. Unlink the current OpenSSL version:
   ```bash
   brew unlink openssl
   ```

3. Link OpenSSL 1.1.x:
   ```bash
   brew link openssl@1.1
   ```

4. Confirm that you have linked OpenSSL 1.1.x:
   ```bash
   openssl version
   ```

5. Run your usual RVM install command:
   ```bash
   rvm install ruby
   ```

6. Confirm the installed Ruby versions:
   ```bash
   rvm list
   ```

   This should display the installed Ruby versions with ARM64 architecture.

## Result

You should see the installed Ruby versions, and you can now use them for your projects.

## Additional Steps

- Install [RVM](https://rvm.io/rvm/install) first!
- Update RVM if necessary:
  ```bash
  rvm get stable
  ```

- Install Ruby:
  ```bash
  rvm install ruby-2.7.2
  ```

- Use Ruby:
  ```bash
  rvm use ruby-2.7.2
  ```

- Bundler:
  The `bundle` command is included with RVM installs of Ruby.
