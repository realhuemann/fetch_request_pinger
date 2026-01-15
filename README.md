# Fetch Request Pinger

A simple tool that allows users to check whether a server is reachable by sending an HTTP `fetch` request using `no-cors` mode.

---

## Usage

1. Paste a valid, full URL (including `http://` or `https://`) into the input field.
2. Click the button to send the request.

---

## How It Works

- The application sends a basic **GET request** to the specified URL using the Fetch API with `no-cors` mode enabled.
- Because `no-cors` restricts access to the response body and headers, the tool does **not** inspect the response contents.
- If the request completes without a network error, the tool infers that the server is reachable from the client machine.

---

## Use Cases

This tool can be useful for:

- Testing basic network connectivity to a server
- Verifying whether firewall or filtering software blocks outbound requests
- Debugging server accessibility issues
- Confirming whether a client machine can contact a server at all

---

## Limitations

- Does not verify HTTP status codes
- Cannot read response data due to `no-cors` restrictions
- A successful request does not guarantee the server is functioning correctly—only that it is reachable
