
# Profile

## Structure

`Profile`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authType` | `string` | Required | The type of Wi-Fi network. Possible values: **wpa-psk**, **wpa2-psk**, **wpa-eap**, **wpa2-eap**. | getAuthType(): string | setAuthType(string authType): void |
| `autoWifi` | `?bool` | Optional | Indicates whether to automatically select the best authentication method available. Does not work on older terminal models. | getAutoWifi(): ?bool | setAutoWifi(?bool autoWifi): void |
| `bssType` | `string` | Required | Use **infra** for infrastructure-based networks. This applies to most networks. Use **adhoc** only if the communication is p2p-based between base stations. | getBssType(): string | setBssType(string bssType): void |
| `channel` | `?int` | Optional | The channel number of the Wi-Fi network. The recommended setting is **0** for automatic channel selection. | getChannel(): ?int | setChannel(?int channel): void |
| `defaultProfile` | `?bool` | Optional | Indicates whether this is your preferred wireless network. If **true**, the terminal will try connecting to this network first. | getDefaultProfile(): ?bool | setDefaultProfile(?bool defaultProfile): void |
| `domainSuffix` | `?string` | Optional | Specifies the server domain name for EAP-TLS and EAP-PEAP WiFi profiles on Android 11 and above. | getDomainSuffix(): ?string | setDomainSuffix(?string domainSuffix): void |
| `eap` | `?string` | Optional | For `authType` **wpa-eap** or **wpa2-eap**. Possible values: **tls**, **peap**, **leap**, **fast** | getEap(): ?string | setEap(?string eap): void |
| `eapCaCert` | [`?File1`](../../doc/models/file-1.md) | Optional | For `authType` **wpa-eap** or **wpa2-eap**. The root certificate from the CA that signed the certificate of the RADIUS server that is part of your wireless network. | getEapCaCert(): ?File1 | setEapCaCert(?File1 eapCaCert): void |
| `eapClientCert` | [`?File2`](../../doc/models/file-2.md) | Optional | For `eap` **tls**. The certificate chain for the terminals. All terminals in the same network will use the same EAP client certificate. | getEapClientCert(): ?File2 | setEapClientCert(?File2 eapClientCert): void |
| `eapClientKey` | [`?File3`](../../doc/models/file-3.md) | Optional | For `eap` **tls**. The RSA private key for the client. Include the lines BEGIN RSA PRIVATE KEY and END RSA PRIVATE KEY. | getEapClientKey(): ?File3 | setEapClientKey(?File3 eapClientKey): void |
| `eapClientPwd` | `?string` | Optional | For `eap` **tls**. The password of the RSA key file, if that file is password-protected. | getEapClientPwd(): ?string | setEapClientPwd(?string eapClientPwd): void |
| `eapIdentity` | `?string` | Optional | For `authType` **wpa-eap** or **wpa2-eap**. The EAP-PEAP username from your MS-CHAP account. Must match the configuration of your RADIUS server. | getEapIdentity(): ?string | setEapIdentity(?string eapIdentity): void |
| `eapIntermediateCert` | [`?File4`](../../doc/models/file-4.md) | Optional | For `eap` **tls**. The EAP intermediate certificate. | getEapIntermediateCert(): ?File4 | setEapIntermediateCert(?File4 eapIntermediateCert): void |
| `eapPwd` | `?string` | Optional | For `eap` **peap**. The EAP-PEAP password from your MS-CHAP account. Must match the configuration of your RADIUS server. | getEapPwd(): ?string | setEapPwd(?string eapPwd): void |
| `hiddenSsid` | `?bool` | Optional | Indicates if the network doesn't broadcast its SSID. Mandatory for Android terminals, because these terminals rely on this setting to be able to connect to any network. | getHiddenSsid(): ?bool | setHiddenSsid(?bool hiddenSsid): void |
| `name` | `?string` | Optional | Your name for the Wi-Fi profile. | getName(): ?string | setName(?string name): void |
| `psk` | `?string` | Optional | For `authType` **wpa-psk or **wpa2-psk**. The password to the wireless network. | getPsk(): ?string | setPsk(?string psk): void |
| `ssid` | `string` | Required | The name of the wireless network. | getSsid(): string | setSsid(string ssid): void |
| `wsec` | `string` | Required | The type of encryption. Possible values: **auto**, **ccmp** (recommended), **tkip** | getWsec(): string | setWsec(string wsec): void |

## Example (as JSON)

```json
{
  "authType": "authType8",
  "autoWifi": false,
  "bssType": "bssType4",
  "channel": 16,
  "defaultProfile": false,
  "domainSuffix": "domainSuffix2",
  "eap": "eap0",
  "ssid": "ssid4",
  "wsec": "wsec6"
}
```

