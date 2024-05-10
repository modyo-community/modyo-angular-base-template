# dynamic-react-base-template
## Requirements:
- node@18+
- npm@10+
- @modyo/cli@latest

## Installation and initial setup
Download or fork this repository, and then:

```console
cd path/to/modyo-angular-base-template
npm i
npm run start
```

### Deploy to Modyo Platform Setup
For deploying your project to Modyo and integrating it with your CI/CD pipeline, follow these steps:
1. Install the [modyo-cli](https://docs.modyo.com/en/platform/channels/cli.html)
```console
npm i -g @modyo/cli
```
2. Change the property name in `package.json` to the name of your project
3. Change the root `id` property to your project name in `public/index.html` and `src/index.tsx`
**Note**: The root id should be _unique_ in your site and it should be written in camelCase.
4. Configure the necessary environment variables in an `.env` file or as part of your CI settings(this project have an `.env.example` that you can use, just remove the extension an you are ready to go!):

```yaml
# For deploying your project to Modyo and integrating it with your CI/CD pipeline
# rename this file to ".env" and update the values with your own configuration.

# Find more information on:
# - Modyo Docs https://docs.modyo.com
# - Modyo Community https://www.modyo.com/community


# Base URL of your Modyo organization
MODYO_ACCOUNT_URL=https://my-org.modyo.cloud/

# Either the host or the ID where you will deploy your micro frontend (not both)
# MODYO_SITE_HOST=my-site
MODYO_SITE_ID=65

# Token for authorizing the deployment, obtained from Modyo
MODYO_TOKEN=gT0ogV43LSy4nV9cYtc_hH0i_rUFa01q-12ptFzoW8

# Major version of the Modyo platform where the deployment will take place (8 or 9)
MODYO_VERSION=10

# Directory containing the micro frontend bundle
MODYO_BUILD_DIRECTORY=dist/modyo-angular-base-template

# Name to identify your Micro Frontend in Modyo
WIDGET_NAME=modyo-angular-base-template

# Directive necessary for safely removing some libraries from the liquid parser
MODYO_DISABLE_LIQUID_REGEX=raw
```

## Learn More
Find more information about microfrontends and configuration details on [Modyo Docs](https://docs.modyo.com) & [Modyo Community](https://www.modyo.com/community)
