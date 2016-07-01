# Qt Additions

This project contains various additions to Qt that aren'tpart of Qt yet.

## QSqliteSettingsFormat: SQLite backstore for QSettings
This backend improves the resiliance of QSettings data against system crashes and disk full conditions.
The example use:
```
// place this into your main function:
QSettings localSettingsObject(
  QSettings::registerFormat("x", SqliteSettingsFormat::readFile, SqliteSettingsFormat::writeFile),
  QSettings::UserScope, "Company", "app");
```

