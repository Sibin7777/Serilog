 string executableDirectory = AppDomain.CurrentDomain.BaseDirectory;
 string logFilePath = Path.Combine(executableDirectory, "log.txt");
 Log.Logger = new LoggerConfiguration()
.WriteTo.File(logFilePath, rollingInterval: RollingInterval.Day)
.CreateLogger();

Log.Error("asfss");
