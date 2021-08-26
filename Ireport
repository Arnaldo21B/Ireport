# Ireport
IREPORT 
--En un diagrama de barras que por años salgan los ingresos obtenidos--
select case 
when año=2020 then '2020'
when año=2021 then '2021'
when año=2022 then '2022'
 end as Año,
sum (precios) as TotalProAño
from factura,mantenimiento,tipo_servicio
group by año order by id

<?xml version="1.0" encoding="UTF-8"?>
<jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports http://jasperreports.sourceforge.net/xsd/jasperreport.xsd" name="ReportePorAñoArnaldo" language="groovy" pageWidth="595" pageHeight="842" columnWidth="535" leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20" uuid="feeede54-4dcd-4a61-a060-598e670ea49b">
	<property name="ireport.zoom" value="1.0"/>
	<property name="ireport.x" value="0"/>
	<property name="ireport.y" value="0"/>
	<queryString language="SQL">
		<![CDATA[select case

when año=2020 then '2020'
when año=2021 then '2021'
when año=2022 then '2022'
 end as Año,
sum (precios) as TotalProAño
from factura,mantenimiento,tipo_servicio
group by año]]>
	</queryString>
	<field name="Año" class="java.lang.String"/>
	<field name="TotalProAño" class="java.math.BigDecimal"/>
	<background>
		<band/>
	</background>
	<title>
		<band height="72">
			<frame>
				<reportElement mode="Opaque" x="-20" y="-20" width="595" height="92" backcolor="#006699" uuid="498791db-fc3c-418f-8223-2007e44eaac0"/>
				<staticText>
					<reportElement x="20" y="20" width="234" height="43" forecolor="#FFFFFF" uuid="0866cc6a-4406-404f-aa9a-f7f11209a92c"/>
					<textElement>
						<font size="14" isBold="true"/>
					</textElement>
					<text><![CDATA[Mantenimiento de Equipos]]></text>
				</staticText>
				<staticText>
					<reportElement x="395" y="43" width="180" height="20" forecolor="#FFFFFF" uuid="fcd12e91-eb1d-4437-a42e-de59dcb33ba7"/>
					<textElement textAlignment="Right">
						<font size="14" isBold="false"/>
					</textElement>
					<text><![CDATA[Reporte Por año]]></text>
				</staticText>
			</frame>
		</band>
	</title>
	<pageHeader>
		<band height="13"/>
	</pageHeader>
	<columnHeader>
		<band height="21">
			<line>
				<reportElement x="-20" y="20" width="595" height="1" forecolor="#666666" uuid="3ff15f48-a9e6-4792-8934-c9a2ec6c5069"/>
			</line>
			<staticText>
				<reportElement mode="Opaque" x="0" y="0" width="277" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="1e4f2ec9-3b27-4714-86b0-d8236f5b1a92"/>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[Año]]></text>
			</staticText>
			<staticText>
				<reportElement mode="Opaque" x="277" y="0" width="277" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="18fb232d-4b2f-4d92-b4ac-02979350ab63"/>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[TotalProAño]]></text>
			</staticText>
		</band>
	</columnHeader>
	<detail>
		<band height="20">
			<line>
				<reportElement positionType="FixRelativeToBottom" x="0" y="19" width="555" height="1" uuid="a3009924-b352-4990-b1e2-2cf1b226c126"/>
			</line>
			<textField isStretchWithOverflow="true">
				<reportElement x="0" y="0" width="277" height="20" uuid="ad6f7d49-9c0b-4328-a0e1-e751d5bdae1d"/>
				<textElement>
					<font size="14"/>
				</textElement>
			</textField>
			<textField isStretchWithOverflow="true">
				<reportElement x="277" y="0" width="277" height="20" uuid="74a9b6e2-30b2-4463-8eeb-702fda9d4390"/>
				<textElement>
					<font size="14"/>
				</textElement>
				<textFieldExpression><![CDATA[$F{TotalProAño}]]></textFieldExpression>
			</textField>
			<componentElement>
				<reportElement x="0" y="0" width="234" height="19" uuid="c0994d80-bb48-44a0-8d58-aa0b11376498"/>
				<jr:barbecue xmlns:jr="http://jasperreports.sourceforge.net/jasperreports/components" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports/components http://jasperreports.sourceforge.net/xsd/components.xsd" type="Monarch" drawText="false" checksumRequired="false">
					<jr:codeExpression><![CDATA[$F{Año}]]></jr:codeExpression>
				</jr:barbecue>
			</componentElement>
		</band>
	</detail>
	<columnFooter>
		<band/>
	</columnFooter>
	<pageFooter>
		<band height="17">
			<textField>
				<reportElement mode="Opaque" x="0" y="4" width="515" height="13" backcolor="#E6E6E6" uuid="e54b2e0b-6121-4b26-9915-f97495e03eb5"/>
				<textElement textAlignment="Right"/>
				<textFieldExpression><![CDATA["Page "+$V{PAGE_NUMBER}+" of"]]></textFieldExpression>
			</textField>
			<textField evaluationTime="Report">
				<reportElement mode="Opaque" x="515" y="4" width="40" height="13" backcolor="#E6E6E6" uuid="93be2aa9-a9b6-440d-a2c7-9c8f45fcf152"/>
				<textFieldExpression><![CDATA[" " + $V{PAGE_NUMBER}]]></textFieldExpression>
			</textField>
			<textField pattern="EEEEE dd MMMMM yyyy">
				<reportElement x="0" y="4" width="100" height="13" uuid="cf9e8884-694c-428d-a527-cc496a62fe86"/>
				<textFieldExpression><![CDATA[new java.util.Date()]]></textFieldExpression>
			</textField>
		</band>
	</pageFooter>
	<summary>
		<band/>
	</summary>
</jasperReport>
