# CloudAssignment

# Structure (provided by AI)
CloudAssignment/
cmd/
 server/
 main.go              # starts the HTTP server, routes
internal/
 handlers/
 status.go            # /status handler
 info.go              # /info/{code} handler
 exchange.go          # /exchange/{code} handler
 router.go            # optional: central route wiring
 clients/
 restcountries.go     # HTTP calls + parsing for REST Countries
 currency.go          # HTTP calls + parsing for Currency API
 httpclient.go        # shared doRequest(), timeouts, error handling
 models/
 restcountries_types.go  # structs matching upstream JSON (only needed fields)
 currency_types.go       # structs matching upstream JSON
 api_types.go            # structs for YOUR responses (status/info/exchange)
 util/
 normalize.go         # uppercase/lowercase country codes, etc.
 errors.go            # helper for JSON error responses
testdata/
restcountries_no.json  # saved example upstream responses for local tests
currency_example.json
README.md
go.mod
