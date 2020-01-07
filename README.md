# TL;DR

- graphql-jit helps
- apollo-server adds overhead
- tracing resolvers kills performance

# Explanation

For further details, please check out [this video](https://www.youtube.com/watch?v=JbV7MCeEPb8).

# Usage

```
git clone https://github.com/benawad/benchmarks
cd benchmarks
npm install
npm start
```

# Benchmarks

duration: 5.02s
connections: 5
pipelining: 1

| Server                                                                                                                                                            | Requests/s | Latency | Throughput/Mb |
| :--                                                                                                                                                               | --:        | :-:     | --:           |
| [fastify-REST](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/fastify-REST.js)                                                         | 6054.0     | 0.29    | 48.42         |
| [fastify-gql+graphql-jit](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/fastify-gql+graphql-jit.js)                                   | 5835.6     | 0.29    | 36.35         |
| [express-REST](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-REST.js)                                                         | 4509.8     | 0.51    | 36.35         |
| [koa+graphql-jit](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/koa+graphql-jit.js)                                                   | 2854.6     | 1.32    | 17.78         |
| [fastify-gql](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/fastify-gql.js)                                                           | 2642.6     | 1.40    | 16.46         |
| [express-graphql+graphql-jit](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-graphql+graphql-jit.js)                           | 2551.0     | 1.44    | 16.05         |
| [express-graphql+graphql-jit+type-graphql](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-graphql+graphql-jit+type-graphql.js) | 2255.0     | 1.62    | 14.19         |
| [yoga-graphql-jit](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/yoga-graphql-jit.js)                                                 | 2223.2     | 1.70    | 0.64          |
| [apollo-server-fastify+graphql-jit](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/apollo-server-fastify+graphql-jit.js)               | 1993.6     | 1.91    | 12.45         |
| [graphql-api-koa](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/graphql-api-koa.js)                                                   | 1816.4     | 2.43    | 11.32         |
| [express-graphql](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-graphql.js)                                                   | 1634.0     | 2.68    | 10.29         |
| [yoga-graphql](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/yoga-graphql.js)                                                         | 1604.4     | 2.77    | 10.06         |
| [express-graphql+type-graphql](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-graphql+type-graphql.js)                         | 1582.2     | 2.71    | 9.96          |
| [type-graphql+async](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/type-graphql+async.js)                                             | 1488.2     | 2.82    | 9.37          |
| [type-graphql+middleware](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/type-graphql+middleware.js)                                   | 1471.4     | 2.87    | 9.26          |
| [type-graphql+async-middleware](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/type-graphql+async-middleware.js)                       | 1434.8     | 2.95    | 9.03          |
| [express-graphql-dd-trace-no-plugin](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-graphql-dd-trace-no-plugin.js)             | 1361.8     | 3.09    | 8.57          |
| [apollo-schema+async](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/apollo-schema+async.js)                                           | 1278.8     | 3.41    | 8.05          |
| [apollo-server-fastify](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/apollo-server-fastify.js)                                       | 1270.6     | 3.41    | 7.94          |
| [apollo-server-express](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/apollo-server-express.js)                                       | 1206.4     | 3.58    | 7.63          |
| [yoga-graphql-trace](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/yoga-graphql-trace.js)                                             | 957.8      | 4.67    | 30.44         |
| [apollo-opentracing](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/apollo-opentracing.js)                                             | 940.4      | 4.74    | 5.95          |
| [apollo-server-express-tracing](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/apollo-server-express-tracing.js)                       | 686.4      | 6.79    | 21.86         |
| [express-graphql-dd-trace](https://github.com/benawad/node-graphql-benchmarks/tree/master/benchmarks/express-graphql-dd-trace.js)                                 | 621.6      | 7.58    | 3.91          |
