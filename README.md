# PageOne Lab MCP catalog

Public discovery metadata and Hermes catalog manifests for PageOne Lab, Inc.'s six hosted MCP services. The services expose public, read-only tools without MCP credentials. Contact: **leo@pageonelab.com**.

| App and documentation | MCP endpoint | Official Registry name |
| --- | --- | --- |
| [Brek - Hotel Wholesale Booking](https://www.brek.com/help/connectors) | `https://mcp.brek.com/mcp` | `io.github.leo9/brek` |
| [HotelUse - Hotel Metasearch](https://www.hoteluse.dev/docs/) | `https://www.hoteluse.dev/mcp/search` | `io.github.leo9/hoteluse` |
| [RoomLast - Last-Minute Hotels](https://www.roomlast.com/help/roomlast-connectors) | `https://mcp.roomlast.com/mcp` | `io.github.leo9/roomlast` |
| [StayForWork - Housing and Hotels for Travel Workers](https://www.stayforwork.com/mcp/docs) | `https://www.stayforwork.com/mcp` | `io.github.leo9/stayforwork` |
| [SOTA2 — AI Solution Rankings](https://www.sota2.com/with-ai) | `https://www.sota2.com/mcp` | `io.github.leo9/sota2` |
| [CareOpenly - Find Senior Living  Communities](https://www.careopenly.com/connectors) | `https://mcp.careopenly.com/mcp` | `io.github.leo9/careopenly` |

## Use with Hermes

The `hermes/<app>/manifest.yaml` files are catalog submissions for maintainer review. Until they are merged into the upstream Hermes catalog, connect a service directly through Hermes's documented custom MCP configuration. For example:

```yaml
mcp_servers:
  brek:
    url: https://mcp.brek.com/mcp
```

Use each service's documentation and privacy policy, and review the usage boundaries in its manifest. Bookings, payments and account actions continue on the service/provider website. SOTA2 reads published rankings and research; CareOpenly reads public community facts and published observations.

## Official MCP Registry publication

Each `servers/<app>/server.json` uses the official remote-server schema and the live MCP implementation version observed during discovery. It describes a hosted endpoint; it does not distribute the server implementation or claim to contain its source code.

The manually dispatched `Publish MCP Registry listings` workflow validates the six records and publishes them through the official `mcp-publisher` using GitHub OIDC. It uses no repository secrets. Public catalog publication is separate from acceptance into any client application's curated directory.
