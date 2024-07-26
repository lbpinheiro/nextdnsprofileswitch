# NextDNS Profile Switch

This repository contains a bash script for quickly switching [NextDNS](https://my.nextdns.io) profiles. The script allows you to set a specific NextDNS profile and restart the `nextdns` service.

## Requirements

- [nextdns](https://github.com/nextdns/nextdns/wiki) must be installed on the system.
- The script must be run as root.

## Usage

1. Edit the `profiles`. Note that the identifier doesn't need to match the exact NextDNS profile names; it is a simple mnemonic.

Example:

```bash
profiles=(
   ["standard"]="9f8d7d"
   ["weird"]="hfyd6c88"
)
```

2. **Run the Script**

Use sudo to execute the script with root privileges. Replace <profile_identifier> with the identifier of the profile you wish to set.

```bash
sudo ./nextdnsprofileswitch <profile_identifier>
```

Example:

```bash
sudo ./nextdnsprofileswitch weird
```

## Notes

- Ensure the script has execute permissions (`chmod +x nextdnsprofileswitch`).
- If nextdns is not installed, the script will provide an appropriate error message.
- The script must be run as root to perform the profile configuration and restart.

## License

This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/license/MIT) file for details
