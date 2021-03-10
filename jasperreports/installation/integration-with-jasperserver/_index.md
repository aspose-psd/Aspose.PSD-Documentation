---
title: Integration with JasperServer
type: docs
weight: 20
url: /jasperreports/integration-with-jasperserver/
---
{{% alert color="primary" %}}
To integrate Aspose.PSD for JasperReports with JasperServer, it is necessary to take several additional steps and update the JasperServer config files. This article explains how.
{{% /alert %}}
1. Add new exporter properties to the %INTALL_DIR%\apache-tomcat\webapps\jasperserver\WEB-INF\flows\viewReportBeans.xml config file.
{{< highlight xml >}}
    <!--JPG-->
    <bean id="reportASJpegExporter" class="com.aspose.psd.jasperreports.jpg.ASReportJpegExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="jpgExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Batch</value>
        </property>
    </bean>

    <bean id="jpgASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="JPG - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="jpgExportParams"/>
        <property name="exportParameters" ref="jpgExportParameters"/>
        <property name="currentExporter" ref="reportASJpegExporter"/>
    </bean>

    <!--BMP-->
    <bean id="reportASBmpExporter" class="com.aspose.psd.jasperreports.bmp.ASReportBmpExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="bmpExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Batch</value>
        </property>
    </bean>

    <bean id="bmpASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="BMP - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="bmpExportParams"/>
        <property name="exportParameters" ref="bmpExportParameters"/>
        <property name="currentExporter" ref="reportASBmpExporter"/>
    </bean>

    <!--GIF-->
    <bean id="reportASGifExporter" class="com.aspose.psd.jasperreports.gif.ASReportGifExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="gifExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Batch</value>
        </property>
    </bean>

    <bean id="gifASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="GIF - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="gifExportParams"/>
        <property name="exportParameters" ref="gifExportParameters"/>
        <property name="currentExporter" ref="reportASGifExporter"/>
    </bean>

    <!--JPG2000-->
    <bean id="reportASJpg2000Exporter" class="com.aspose.psd.jasperreports.jpg2000.ASReportJpeg2000Exporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="jpg2000ExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Batch</value>
        </property>
    </bean>

    <bean id="jpg2000ASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="JPG2000 - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="jpg2000ExportParams"/>
        <property name="exportParameters" ref="jpg2000ExportParameters"/>
        <property name="currentExporter" ref="reportASJpg2000Exporter"/>
    </bean>

    <!--PDF-->
    <bean id="reportASPdfExporter" class="com.aspose.psd.jasperreports.pdf.ASReportPdfExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="pdfASExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Multipage</value>
        </property>
    </bean>

    <bean id="pdfASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="PDF - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="pdfExportParams"/>
        <property name="exportParameters" ref="pdfASExportParameters"/>
        <property name="currentExporter" ref="reportASPdfExporter"/>
    </bean>

    <!--PNG-->
    <bean id="reportASPngExporter" class="com.aspose.psd.jasperreports.png.ASReportPngExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="pngExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Batch</value>
        </property>
    </bean>

    <bean id="pngASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="PNG - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="pngExportParams"/>
        <property name="exportParameters" ref="pngExportParameters"/>
        <property name="currentExporter" ref="reportASPngExporter"/>
    </bean>

    <!--PSD-->
    <bean id="reportASPsdExporter" class="com.aspose.psd.jasperreports.psd.ASReportPsdExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="psdExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Batch</value>
        </property>
    </bean>

    <bean id="psdASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="PSD - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="psdExportParams"/>
        <property name="exportParameters" ref="psdExportParameters"/>
        <property name="currentExporter" ref="reportASPsdExporter"/>
    </bean>

    <!--TIFF-->
    <bean id="reportASTiffExporter" class="com.aspose.psd.jasperreports.tiff.ASReportTiffExporter"
          parent="baseReportExporter">
        <property name="exportParameters" ref="tiffExportParameters"/>
        <property name="exportMode">
            <value type="com.aspose.psd.jasperreports.common.ExportMode">Multipage</value>
        </property>
    </bean>

    <bean id="tiffASExporterParameters" class="com.jaspersoft.jasperserver.war.action.ExporterConfigurationBean">
        <property name="descriptionKey" value="TIFF - Image export from Aspose.PSD"/>
        <property name="parameterDialogName" value="tiffExportParams"/>
        <property name="exportParameters" ref="tiffExportParameters"/>
        <property name="currentExporter" ref="reportASTiffExporter"/>
    </bean>
{{< /highlight >}}

    To change the mode of the export use property with name "exportMode" and put the value according to the desired mode. 
For example:
{{< highlight xml >}}
    <property name="exportMode">
        <value type="com.aspose.psd.jasperreports.common.ExportMode">SinglePage</value>
    </property>
{{< /highlight >}}
    You can change the value of the property to Batch, SinglePage or Multipage using com.aspose.psd.jasperreports.common.ExportMode enum type.

2. Locate the <util:map id="exporterConfigMap"> element in the %INTALL_DIR%\\apache-tomcat\webapps\jasperserver\WEB-INF\flows\viewReportBeans.xml file and add the following lines:
{{< highlight xml >}}
    <util:map id="exporterConfigMap">
        <!-- comment/uncomment any of the lines below if you want related exporters 
        	 to be excluded/included in the viewer's exporters list
        	 Note: separate configuration for iPad 'exportersSupportedByiPad'
        	 -->
        	 
        <entry key="pdf" value-ref="pdfExporterConfiguration"/>
        <entry key="xls" value-ref="xlsExporterConfiguration"/>
        <entry key="xlsNoPag" value-ref="xlsNoPaginationExporterConfiguration"/>
        <entry key="csv" value-ref="csvExporterConfiguration"/>
        <entry key="docx" value-ref="docxExporterConfiguration"/>
        <entry key="rtf" value-ref="rtfExporterConfiguration"/>
        <entry key="odt" value-ref="odtExporterConfiguration"/>
        <entry key="ods" value-ref="odsExporterConfiguration"/>
        <entry key="xlsx" value-ref="xlsxExporterConfiguration"/>
        <entry key="xlsxNoPag" value-ref="xlsxNoPaginationExporterConfiguration"/>
        <entry key="pptx" value-ref="pptxExporterConfiguration"/>
        <!-- 
        <entry key="txt" value-ref="txtExporterConfiguration"/>
        -->
		
			<!-- add this entries to exporterConfigMap -->
			<!-- Aspose.PSD JasperReports START -->
		<entry key="as_jpg" value-ref="jpgASExporterParameters"/>
		<entry key="as_bmp" value-ref="bmpASExporterParameters"/>
		<entry key="as_gif" value-ref="gifASExporterParameters"/>
		<entry key="as_jpg2000" value-ref="jpg2000ASExporterParameters"/>
		<entry key="as_pdf" value-ref="pdfASExporterParameters"/>
		<entry key="as_png" value-ref="pngASExporterParameters"/>
		<entry key="as_psd" value-ref="psdASExporterParameters"/>
		<entry key="as_tiff" value-ref="tiffASExporterParameters"/>
		<!-- Aspose.PSD for JasperReports END -->
    </util:map>
{{< /highlight >}}
3. Copy aspose-psd-jasperreports-xx.xx.jar to %INTALL_DIR%\apache-tomcat\webapps\jasperserver\WEB-INF\lib.
4. To use exporting features, update %INTALL_DIR%\apache-tomcat\webapps\jasperserver\WEB-INF\applicationContext.xml as below.
{{< highlight xml >}}
    <bean id="jpgExportParameters" class="com.aspose.psd.jasperreports.jpg.ASJpegExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="bmpExportParameters" class="com.aspose.psd.jasperreports.bmp.ASBmpExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="gifExportParameters" class="com.aspose.psd.jasperreports.gif.ASGifExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="jpg2000ExportParameters" class="com.aspose.psd.jasperreports.jpg2000.ASJpeg2000ExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="pdfASExportParameters" class="com.aspose.psd.jasperreports.pdf.ASPdfExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="pngExportParameters" class="com.aspose.psd.jasperreports.png.ASPngExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="psdExportParameters" class="com.aspose.psd.jasperreports.psd.ASPsdExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>

	<bean id="tiffExportParameters" class="com.aspose.psd.jasperreports.tiff.ASTiffExportParametersBean">
	<!--        Uncomment and modify to apply a license. Check the license path.
	<property name="license" value="C:/Aspose.PSD.JasperReports.lic"/>
	-->
	</bean>
{{< /highlight >}}

5. Restart JasperReports Server and open any report to view. If the previous steps were performed properly, you will see additional choices in the list of export formats.
![todo:image_alt_text](ExportReportView.jpg)

If you do not see additional formats (icons or choices), please check log files in \apache-tomcat\logs directory.