---
title: Client Properties (4.x)
category: configuration
order: 3
---

<!-- WARNING: Do not edit this file. It is a generated file that is copied from Accumulo build (from core/target/generated-docs) -->
<!-- Generated by : org.apache.accumulo.core.conf.ClientConfigGenerate$Markdown -->

Below are properties set in `accumulo-client.properties` that configure [Accumulo clients]({{ page.docs_baseurl }}/getting-started/clients#connecting). All properties have been part of the API since 2.0.0 (unless otherwise specified):

| Property | Default value | Since | Description |
|----------|---------------|-------|-------------|
| <a name="instance_name" class="prop"></a> instance.name | *empty* | 2.0.0 | Name of Accumulo instance to connect to |
| <a name="instance_zookeepers" class="prop"></a> instance.zookeepers | localhost:2181 | 2.0.0 | Zookeeper connection information for Accumulo instance |
| <a name="instance_zookeepers_timeout" class="prop"></a> instance.zookeepers.timeout | 30s | 2.0.0 | Zookeeper session timeout |
| <a name="auth_type" class="prop"></a> auth.type | password | 2.0.0 | Authentication method (i.e password, kerberos, PasswordToken, KerberosToken, etc) |
| <a name="auth_principal" class="prop"></a> auth.principal | *empty* | 2.0.0 | Accumulo principal/username for chosen authentication method |
| <a name="auth_token" class="prop"></a> auth.token | *empty* | 2.0.0 | Authentication token (ex. mypassword, /path/to/keytab) |
| <a name="batch_writer_durability" class="prop"></a> batch.writer.durability | default | 2.0.0 | The durability used to write to the write-ahead log. Legal values are: none, which skips the write-ahead log; log, which sends the data to the write-ahead log, but does nothing to make it durable; flush, which pushes data to the file system; and sync, which ensures the data is written to disk. Setting this property will change the durability for the BatchWriter session. A value of "default" will use the table's durability setting.  |
| <a name="batch_writer_latency_max" class="prop"></a> batch.writer.latency.max | 120s | 2.0.0 | Max amount of time (in seconds) to hold data in memory before flushing it |
| <a name="batch_writer_memory_max" class="prop"></a> batch.writer.memory.max | 50M | 2.0.0 | Max memory (in bytes) to batch before writing |
| <a name="batch_writer_threads_max" class="prop"></a> batch.writer.threads.max | 3 | 2.0.0 | Maximum number of threads to use for writing data to tablet servers. |
| <a name="batch_writer_timeout_max" class="prop"></a> batch.writer.timeout.max | 0 | 2.0.0 | Max amount of time (in seconds) an unresponsive server will be re-tried. An exception is thrown when this timeout is exceeded. Set to zero for no timeout. |
| <a name="batch_scanner_num_query_threads" class="prop"></a> batch.scanner.num.query.threads | 3 | 2.0.0 | Number of concurrent query threads to spawn for querying |
| <a name="scanner_batch_size" class="prop"></a> scanner.batch.size | 1000 | 2.0.0 | Number of key/value pairs that will be fetched at time from tablet server |
| <a name="ssl_enabled" class="prop"></a> ssl.enabled | false |  | Enable SSL for client RPC |
| <a name="ssl_keystore_password" class="prop"></a> ssl.keystore.password | *empty* |  | Password used to encrypt keystore |
| <a name="ssl_keystore_path" class="prop"></a> ssl.keystore.path | *empty* | 2.0.0 | Path to SSL keystore file |
| <a name="ssl_keystore_type" class="prop"></a> ssl.keystore.type | jks |  | Type of SSL keystore |
| <a name="ssl_truststore_password" class="prop"></a> ssl.truststore.password | *empty* |  | Password used to encrypt truststore |
| <a name="ssl_truststore_path" class="prop"></a> ssl.truststore.path | *empty* | 2.0.0 | Path to SSL truststore file |
| <a name="ssl_truststore_type" class="prop"></a> ssl.truststore.type | jks |  | Type of SSL truststore |
| <a name="ssl_use_jsse" class="prop"></a> ssl.use.jsse | false |  | Use JSSE system properties to configure SSL |
| <a name="sasl_enabled" class="prop"></a> sasl.enabled | false |  | Enable SASL for client RPC |
| <a name="sasl_kerberos_server_primary" class="prop"></a> sasl.kerberos.server.primary | accumulo |  | Kerberos principal/primary that Accumulo servers use to login |
| <a name="sasl_qop" class="prop"></a> sasl.qop | auth |  | SASL quality of protection. Valid values are 'auth', 'auth-int', and 'auth-conf' |
