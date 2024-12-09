cxx_library(
    name = "timer_lib",
    srcs = [
        "timer/lst_timer.cpp",
    ],
    compiler_flags = [
        "-O2",
    ],
)

cxx_library(
    name = "http_lib",
    srcs = [
        "http/http_conn.cpp",
    ],
    compiler_flags = [
        "-O2",
    ],
)

cxx_library(
    name = "log_lib",
    srcs = [
        "log/log.cpp",
    ],
    compiler_flags = [
        "-O2",
    ],
)

cxx_library(
    name = "sql_lib",
    srcs = [
        "CGImysql/sql_connection_pool.cpp",
    ],
    compiler_flags = [
        "-O2",
    ],
)

cxx_library(
    name = "webserver_lib",
    srcs = [
        "webserver.cpp",
        "config.cpp",
    ],
    compiler_flags = [
        "-O2",
    ],
)

cxx_binary(
    name = "server",
    srcs = [
        "main.cpp",
    ],
    compiler_flags = [
        "-O2",
    ],
    deps = [
        ":timer_lib",
        ":http_lib",
        ":log_lib",
        ":sql_lib",
        ":webserver_lib",
    ],
    linker_flags = [
        "-lpthread",
        "-lmysqlclient",
    ],
)
