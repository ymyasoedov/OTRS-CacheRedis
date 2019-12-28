# CacheRedis
Implementation OTRS cache on Redis.

## Building OPM package

```
$OTRS_HOME/bin/otrs.Console.pl Dev::Package::Build --module-directory <path_to_dir> <path_to_sopm> <where_to_put_opm>
```

## Installing

```
$OTRS_HOME/bin/otrs.Console.pl Admin::Package::Install <path_to_built_opm>
```

## Configuration

| Setting                       | Description                | Default value  |
| ----------------------------- | -------------------------- | -------------- |
| Cache::Redis###Server         | Redis server URL           | 127.0.0.1:6379 |
| Cache::Redis###DatabaseNumber | Number of logical database | 0              |
| Cache::Redis###RedisFast      | Use or not Redis::Fast     | 0              |

### Redis or Redis::Fast

You can choose what Redis module to being used: `Redis` or `Redis::Fast` (it's compatible with Redis, but **~2x faster**).
