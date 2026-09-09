# Beeper config

A personal Beeper Desktop theme inspired by Messages on macOS. The stylesheet uses a solid conversation background and a translucent sidebar, with a floating glass composer.

## Install on macOS

Back up your existing `custom.css` before replacing it. If the destination is a Nix-managed symlink, move the symlink aside first; do not write through it into the Nix store.

From this repository:

```sh
cp custom.css "$HOME/Library/Application Support/BeeperTexts/custom.css"
```

In Beeper's command bar, run **Reload custom CSS**.

To revert, restore your backup at the same path and reload again. This repository does not change Nix configuration.

## Customize

Edit the variables near the top of `custom.css`:

| Variable | Purpose |
| --- | --- |
| `--im-sidebar-width` | Requested sidebar width |
| `--im-message-size` | Message and input text size |
| `--im-message-weight` | Message and input text weight |
| `--im-control-fill` | Shared input and plus-button tint |
| `--im-control-filter` | Shared glass blur |
| `--im-sidebar-glass` | Focused sidebar fill |
| `--im-sidebar-inactive` | Unfocused sidebar fill |

Light and dark appearances have separate colors. The theme hides the send button and sidebar search/new-chat buttons; use Beeper's keyboard shortcuts for those actions. Native macOS window buttons remain visible.

## Limits

Selectors were checked against Beeper Desktop 4.3.89. App updates may change them. This is a CSS approximation, not an exact copy of Messages.

The sidebar width remains unverified in the live layout. The floating composer reserves space for a single-line draft; expanded drafts and attachment trays need further testing. Reaction placement also needs testing across message types.

Delivery status is unchanged. The theme does not turn a sent message into a delivered message.

## Check CSS syntax

With Bun installed:

```sh
bun build custom.css --outfile /tmp/beeper-config.checked.css
```

This checks CSS compilation, not live rendering or selector matches.

## Authorship

Created with an AI agent via Codex.
