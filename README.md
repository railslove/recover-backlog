<p align="center">
  <img src="https://raw.githubusercontent.com/railslove/rcvr-app/master/.github/checkmark.png" width="95" height="87" alt="">
</p>

<h1 align="center">rcvr.app Backlog</h1>

<p align="center">
  <a href="https://rcvr.app">rcvr.app</a> – client app for <a href="https://www.recoverapp.de">recover</a> – a product by <a href="https://railslove.com">Railslove</a>
</p>

- [Intro](#intro)
- [How does rcvr.app work?](#how-does-rcvrapp-work)
- [Background](#background)
- [Contribute](#contribute)
- [License](#license)

# Recoverapp: Backlog

<a href="https://github.com/railslove/recover-backlog/issues" title="Open Issues"><img src="https://img.shields.io/github/issues/railslove/recover-backlog"></a>

## Intro

Due to COVID-19, many localities, like bars and restaurants, must keep track of their guest. So, in the case of infection, the public health department can trace contact persons using this data.

The German government suggested a very old-school way on how to achieve this. Owners should put a printed document on each table, and guests have to write down their data with a pen, visible to everyone.

**We know we can do better.** Those lists are annoying for everyone, and especially a big privacy concern.

With **recover**, guests scan a QR Code with their phone and enter their contact details, which will be encrypted on their device and stored on our server. Only the business owner can decrypt this data, and only when the public health department requests it.

## How does rcvr.app work?

When an owner signs up, a key pair will be generated on their device. The owner needs to safely store the private key by saving it inside a password manager or writing it on a piece of paper and putting it in a physical safe. This private key is required to decrypt the data of the guests.

The public part of this key pair is embedded inside the QR Code, together with a unique identifier for each table.

When the public health department requests data for a specific time range from an owner, we will send them the guest's encrypted data from this period. The owner can then decrypt this data using his private key and send it to the public health department.

When a guest checks in, a random ID will be saved on the guest's device. **recover** will provide a public feed of all check-in IDs in danger of a COVID-19 infection. The IDs can be public because they cannot be traced back to a person. Only the guest's device knows if one of the stored IDs is also inside this public feed. If this is the case, we can notify the guest of the potential infection.

## Background

**recover** was initially developed during one weekend. We noticed the urgency and needs of business owners and wanted to provide a solution. A special thanks goes to everyone who helped and consulted us to achieve our goal in this short amount of time.

## Contribute

This Backlog repository cointains only the [Issues](https://github.com/railslove/recover-backlog/issues) which are planned for development in our [Project Board](https://github.com/railslove/recover-backlog/projects/1).

## License

**rcvr.app** is open-source and free software released under the [GNU AGPL](https://github.com/railslove/rcvr-app/blob/master/LICENSE) (GNU Affero General Public License v3.0). We, [Railslove GmbH](https://railslove.com/), are committed to ensuring that it will remain a free and open-source project.

---

<p align="center">
  Made with 💚 in Cologne
</p>
