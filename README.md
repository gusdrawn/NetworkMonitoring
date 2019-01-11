![0]

# NetworkMonitoring

# EJECUCION

Ejecutar Modo Administrador

Set-ExecutionPolicy RemoteSigned
(new-object Net.WebClient).DownloadString("https://aka.ms/AzureCT") | Invoke-Expression
Install-LinkPerformance
Y
Get-LinkPerformance -RemoteHost X.X.X.X

Iperf -s <-USA PUERTO 5201

**Azure / NetworkMonitoring** is a repository for open source Azure network monitoring tools. Each tool or collection of tools lives in a folder under the main NetworkMonitoring repo.

The current tools/tool-sets are:
#### AzureCT
The Azure Connectivity Toolkit ([AzureCT][AzureCT]) is a PowerShell module and collection of server side web pages will test, generate, collect, store, and display performance and availability statistics of the network between you and Azure. The two main areas of functionality are:
 - A network availability test (Get-AzureNetworkAvailability) that runs pings and traceroutes over an extended period of time to show end to end availability and hop latency.
 - A bandwidth and latency tester (Get-LinkPerformance) that runs a series of iPerf3 load tests while concurently doing a TCP ping to show latency under various loads.

#### LogConverter
[LogConverter][LogConverter] contains code for downloading operational network logs and converting them to .CSV files. Files can then be uploaded to Power BI for analysis.

<!--Image References-->
[0]: ./AzureCT/media/AzureNMT.png "Azure Network Monitoring Tools"

<!--Link References-->
[LogConverter]: https://github.com/Azure/NetworkMonitoring/tree/master/LogConverter "LogConverter tree"
[AzureCT]: https://github.com/Azure/NetworkMonitoring/tree/master/AzureCT "AzureCT tree"
