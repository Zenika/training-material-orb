# Orb Source

Orbs are shipped as individual `orb.yml` files, however, to make development easier, it is possible to author an orb in _unpacked_ form, which can be _packed_ with the CircleCI CLI and published.

The default `.circleci/config.yml` file contains the configuration code needed to automatically pack, test, and deploy any changes made to the contents of the orb source in this directory.

## @orb.yml

This is the entry point for our orb "tree", which becomes our `orb.yml` file later.

Within the `@orb.yml` we generally specify 4 configuration keys

**Keys**

1. **version**
    Specify version 2.1 for orb-compatible configuration `version: 2.1`
2. **description**
    Give your orb a description. Shown within the CLI and orb registry
3. **display**
    Specify the `home_url` referencing documentation or product URL, and `source_url` linking to the orb's source repository.
4. **orbs**
    (optional) Some orbs may depend on other orbs. Import them here.

## Publication de l'orb

La publication utilise le contexte CircleCI `orb-publishing`, qui doit contenir une variable d'environnement `CIRCLE_TOKEN`.

CircleCI ne propose pas de token au niveau de l'organisation. Le token doit être un **Personal API Token** d'un compte utilisateur ayant les droits `Admin` sur l'organisation. La pratique recommandée est de créer un compte de service dédié (ex. `zenika-bot`) et de stocker son token dans le contexte `orb-publishing`.

Pour créer le token : **User Settings** > **Personal API Tokens** > **Create New Token**.

Pour configurer le contexte : **Organization Settings** > **Contexts** > `orb-publishing` > ajouter la variable `CIRCLE_TOKEN`.

## See:
 - [Orb Author Intro](https://circleci.com/docs/2.0/orb-author-intro/#section=configuration)
 - [Reusable Configuration](https://circleci.com/docs/2.0/reusing-config)
 - [Managing API tokens](https://circleci.com/docs/guides/toolkit/managing-api-tokens/)
