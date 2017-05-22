



## Foundation, Formatter, Date

iOS | Formatter | func string
--|--|--
2|[`DateFormatter`](https://developer.apple.com/reference/foundation/dateformatter)|func string(from date: Date) -> String
10| [`ISO8601DateFormatter`](https://developer.apple.com/reference/foundation/iso8601dateformatter) | func string(from date: Date) -> String
8|[`DateComponentsFormatter`](https://developer.apple.com/reference/foundation/datecomponentsformatter) | func string(from components: DateComponents) -> String? <br> func string(from startDate: Date, to endDate: Date) -> String? <br> func string(from ti: TimeInterval) -> String? <br> func string(for obj: Any?) -> String?
8|[`DateIntervalFormatter`](https://developer.apple.com/reference/foundation/dateintervalformatter) | func string(from fromDate: Date, to toDate: Date) -> String <br> func string(from dateInterval: DateInterval) -> String? // iOS 10
