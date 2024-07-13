# Java Time API Overview

The java.time package, introduced in Java 8, provides a comprehensive set of classes for working with date and time. This package is based on the ISO-8601 calendar system and includes classes for handling different aspects of date and time, such as:

- LocalDate: Represents a date (year, month, day) without a time zone.
- LocalTime: Represents a time (hours, minutes, seconds, nanoseconds) without a date and time zone.
- LocalDateTime: Combines date and time without a time zone.
- ZonedDateTime: Combines date and time with a time zone.
- Instant: Represents a point in time (timestamp) in UTC.

## LocalDate

Represents a date without a time zone. It is useful for representing dates such as birthdays, holidays, etc.

```java
import java.time.LocalDate;

public class LocalDateExample {
    public static void main(String[] args) {
        // Current date
        LocalDate today = LocalDate.now();
        System.out.println("Current date: " + today);

        // Specific date
        LocalDate specificDate = LocalDate.of(2023, 7, 13);
        System.out.println("Specific date: " + specificDate);

        // Parsing date from string
        LocalDate parsedDate = LocalDate.parse("2023-07-13");
        System.out.println("Parsed date: " + parsedDate);
    }
}
```

## LocalTime

Represents a time without a date and time zone. It is useful for representing times of the day such as office hours, meeting times, etc.

```java
import java.time.LocalTime;

public class LocalTimeExample {
    public static void main(String[] args) {
        // Current time
        LocalTime now = LocalTime.now();
        System.out.println("Current time: " + now);

        // Specific time
        LocalTime specificTime = LocalTime.of(10, 15, 30);
        System.out.println("Specific time: " + specificTime);

        // Parsing time from string
        LocalTime parsedTime = LocalTime.parse("10:15:30");
        System.out.println("Parsed time: " + parsedTime);
    }
}
```

## LocalDateTime

Combines LocalDate and LocalTime without a time zone. It is useful for representing a specific date and time, such as a timestamp in local time.

```java
import java.time.LocalDateTime;

public class LocalDateTimeExample {
    public static void main(String[] args) {
        // Current date and time
        LocalDateTime now = LocalDateTime.now();
        System.out.println("Current date and time: " + now);

        // Specific date and time
        LocalDateTime specificDateTime = LocalDateTime.of(2023, 7, 13, 10, 15, 30);
        System.out.println("Specific date and time: " + specificDateTime);

        // Parsing date and time from string
        LocalDateTime parsedDateTime = LocalDateTime.parse("2023-07-13T10:15:30");
        System.out.println("Parsed date and time: " + parsedDateTime);
    }
}
```

## ZonedDateTime

Combines LocalDateTime with a time zone. It is useful for representing a specific date and time in a specific time zone.

```java
import java.time.ZonedDateTime;
import java.time.ZoneId;

public class ZonedDateTimeExample {
    public static void main(String[] args) {
        // Current date and time with system default time zone
        ZonedDateTime now = ZonedDateTime.now();
        System.out.println("Current date and time with time zone: " + now);

        // Specific date and time with a time zone
        ZonedDateTime specificZonedDateTime = ZonedDateTime.of(
            2023, 7, 13, 10, 15, 30, 0, 
            ZoneId.of("America/New_York")
        );

        System.out.println("Specific date and time with time zone: " + specificZonedDateTime);

        // Parsing date and time with time zone from string
        ZonedDateTime parsedZonedDateTime = ZonedDateTime.parse("2023-07-13T10:15:30-04:00[America/New_York]");
        System.out.println("Parsed date and time with time zone: " + parsedZonedDateTime);
    }
}
```

## Instant

Represents a point in time (timestamp) in UTC. It is useful for representing timestamps and performing arithmetic with durations.

```java
import java.time.Instant;

public class InstantExample {
    public static void main(String[] args) {
        // Current timestamp
        Instant now = Instant.now();
        System.out.println("Current timestamp: " + now);

        // Specific timestamp
        Instant specificInstant = Instant.ofEpochSecond(1626114930);
        System.out.println("Specific timestamp: " + specificInstant);

        // Parsing timestamp from string
        Instant parsedInstant = Instant.parse("2023-07-13T14:15:30.00Z");
        System.out.println("Parsed timestamp: " + parsedInstant);
    }
}
```

## DateTimeFormatter

It is used to format and parse date-time objects. It supports a variety of predefined and custom patterns.

```java
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;

public class DateTimeFormatterExample {
    public static void main(String[] args) {
        LocalDateTime dateTime = LocalDateTime.now();

        // Predefined formatter
        DateTimeFormatter isoFormatter = DateTimeFormatter.ISO_DATE_TIME;
        System.out.println("ISO format: " + dateTime.format(isoFormatter));

        // Custom formatter
        DateTimeFormatter customFormatter = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
        System.out.println("Custom format: " + dateTime.format(customFormatter));

        // Parsing using custom formatter
        String dateTimeString = "2023-07-13 10:15:30";
        LocalDateTime parsedDateTime = LocalDateTime.parse(dateTimeString, customFormatter);
        System.out.println("Parsed date and time: " + parsedDateTime);
    }
}
```

## Adding and Subtracting Time

Java Time API provides methods for adding and subtracting time units.

```java
import java.time.LocalDate;
import java.time.LocalTime;
import java.time.LocalDateTime;

public class AddingSubtractingTimeExample {
    public static void main(String[] args) {
        LocalDate date = LocalDate.now();
        LocalTime time = LocalTime.now();
        LocalDateTime dateTime = LocalDateTime.now();

        // Adding time
        LocalDate tomorrow = date.plusDays(1);
        LocalTime inAnHour = time.plusHours(1);
        LocalDateTime nextWeek = dateTime.plusWeeks(1);

        System.out.println("Tomorrow: " + tomorrow);
        System.out.println("In an hour: " + inAnHour);
        System.out.println("Next week: " + nextWeek);

        // Subtracting time
        LocalDate yesterday = date.minusDays(1);
        LocalTime anHourAgo = time.minusHours(1);
        LocalDateTime lastWeek = dateTime.minusWeeks(1);

        System.out.println("Yesterday: " + yesterday);
        System.out.println("An hour ago: " + anHourAgo);
        System.out.println("Last week: " + lastWeek);
    }
}
```

## Comparing Dates and Times

Java Time API provides methods for comparing date-time objects.

```java
import java.time.LocalDate;
import java.time.LocalDateTime;

public class ComparingDatesTimesExample {
    public static void main(String[] args) {
        LocalDate date1 = LocalDate.of(2023, 7, 13);
        LocalDate date2 = LocalDate.of(2023, 7, 14);

        LocalDateTime dateTime1 = LocalDateTime.of(2023, 7, 13, 10, 15);
        LocalDateTime dateTime2 = LocalDateTime.of(2023, 7, 13, 10, 20);

        // Comparing dates
        boolean isBefore = date1.isBefore(date2);
        boolean isAfter = date1.isAfter(date2);
        boolean isEqual = date1.isEqual(date2);

        System.out.println("Date1 is before Date2: " + isBefore);
        System.out.println("Date1 is after Date2: " + isAfter);
        System.out.println("Date1 is equal to Date2: " + isEqual);

        // Comparing date-times
        boolean isDateTimeBefore = dateTime1.isBefore(dateTime2);
        boolean isDateTimeAfter = dateTime1.isAfter(dateTime2);
        boolean isDateTimeEqual = dateTime1.isEqual(dateTime2);

        System.out.println("DateTime1 is before DateTime2: " + isDateTimeBefore);
        System.out.println("DateTime1 is after DateTime2: " + isDateTimeAfter);
        System.out.println("DateTime1 is equal to DateTime2: " + isDateTimeEqual);
    }
}
```

## Legacy Date and Calendar Classes

Java also includes older classes such as Date and Calendar, but they are not recommended for new projects.

```java
import java.util.Date;
import java.util.Calendar;

public class LegacyDateCalendarExample {
    public static void main(String[] args) {
        // Date
        Date legacyDate = new Date();
        System.out.println("Legacy date: " + legacyDate);

        // Calendar
        Calendar calendar = Calendar.getInstance();
        calendar.set(2023, Calendar.JULY, 13, 10, 15, 30);
        Date calendarDate = calendar.getTime();
        System.out.println("Calendar date: " + calendarDate);
    }
}
```