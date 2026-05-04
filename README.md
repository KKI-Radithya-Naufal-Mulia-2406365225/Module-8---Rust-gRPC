1. Unary is simple one request and one response like when we pay. Server streaming send many response for one request like history, and bi-directional can send many message both way same time. Unary is the best for simple task but streaming is better for big data or chat.
2. We must use TLS for encryption so data is safe when moving. It is important to check who is the user before they use service. We also need to limit what user can do in the app.
3. It is difficult because we must keep connection alive for long time. If internet is bad, we need to handle disconnect so the app still work. Managing many messages at same time is also very hard.
4. It is good because it change tokio channel into gRPC stream easily. But, we must be careful with channel size so we don't lose data.
5. We can split code into many files to make it clean. This help us reuse code for different service and for upcoming development.
6. We must add code to check if user have enough money for payment. Also need to handle many error cases so the server not crash.
7. gRPC make it easy for different language to talk each other with protobuf. It change how we make system to be faster.
8. HTTP/2 is very fast because it send many data in one connection. It is better than HTTP/1.1 because it use binary format. But it is harder to read the data for debugging.
9. REST is slow because it must wait for response every time we ask. gRPC bi-directional allow data to move both side anytime so it is very fast for talk. Which will make an app like chat works better and faster.
10. Protocol Buffers use schema so we know what data we get and it is safe. JSON is easy to change but can have error if data type is wrong. Schema also make data small and fast to send.