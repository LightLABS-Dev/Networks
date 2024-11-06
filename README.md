# Networks Repository

This repository contains a collection of **IBC path relays** for the PRYSM Network testnet. Each file details specific IBC paths and the operators responsible for maintaining these paths. 

## Structure

Each JSON file should follow this structure:

```json
{
  "chain_2": {
    "chain_name": "prysm",
    "client_id": "07-tendermint-21",
    "connection_id": "connection-14"
  },
  "chain_1": {
    "chain_name": "elys",
    "client_id": "07-tendermint-118",
    "connection_id": "connection-80"
  },
  "channels": [
    {
      "chain_1": {
        "channel_id": "channel-9",
        "port_id": "transfer"
      },
      "chain_2": {
        "channel_id": "channel-52",
        "port_id": "transfer"
      },
      "ordering": "unordered",
      "version": "ics20-1",
      "tags": {
        "status": "live",
        "preferred": true
      }
    }
  ],
  "operators": [
    {
      "discord": {
        "id": "123456789012345678",
        "handle": "Operator1"
      }
    },
    {
      "discord": {
        "id": "987654321098765432",
        "handle": "Operator2"
      }
    }
  ]
}
```

### Example

The structure above represents an IBC relay path from **Elys** to **PRYSM Network**, with `Operator1` and `Operator2` responsible for the path.

## Adding New Paths

To contribute a new IBC path relay:

1. **Create a JSON file** in the repository with the appropriate structure shown above.
2. **Add the file** to this repository with a descriptive name matching the path, such as `elys-prysm.json`.
3. **Submit a pull request** with your new path and ensure it follows the structure and naming conventions.

## Monitoring Incidents

If you would like to be notified of incidents related to the paths you maintain:

- Add your **Discord ID** and **handle** in the `operators` array of the relevant JSON file.

Adding your information will ensure you’re pinged in the **Relay Monitoring** channel in case of any incidents affecting your paths.

## Contact

For questions or issues related to this repository, please reach out to the PRYSM Network team on our official Discord or email at contact@lightlabs.dev

--- 
