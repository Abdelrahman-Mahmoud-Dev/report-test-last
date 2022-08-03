<template>
  <div id="viewer-host" >
        <Viewer :report="{ Uri: './assets/reports/Untitled.rdlx-json' }" />
  </div>
</template>

<script>
import { Viewer } from "@grapecity/activereports-vue";
// eslint-disable-next-line
import "@grapecity/activereports/pdfexport";
import "@grapecity/activereports/htmlexport";
import "@grapecity/activereports/tabulardataexport";

export default {
  name: "App",
  components: {
   Viewer,
  },
  // data() {
  //   return {
  //     availableExports: ['pdf', 'html', 'tabular-data'],
  //     previewMode: true,
  //     reportsList: reportLabels,
  //     currentReportIndex: undefined,
  //     currentThemeIndex: undefined,
  //     reportsMap: reportsMap,
  //     themeList: themeList,
  //     styles: "",
  //   };
  // },
  // mounted() {
  //   const viewerInstance = this.$refs.reportViewer.Viewer();
  //   viewerInstance.toolbar.addItem({
  //     key: "$openDesigner",
  //     text: "Edit in Designer",
  //     iconCssClass: "mdi mdi-pencil",
  //     enabled: true,
  //     action: () => {
  //       this.previewMode = false;
  //     },
  //   });
  //   // Setting the toolbar layout
  //   viewerInstance.toolbar.updateLayout({
  //     default: [
  //       "$openDesigner",
  //       "$split",
  //       "$navigation",
  //       "$split",
  //       "$refresh",
  //       "$split",
  //       "$history",
  //       "$split",
  //       "$zoom",
  //       "$fullscreen",
  //       "$split",
  //       "$print",
  //       "$split",
  //       "$singlepagemode",
  //       "$continuousmode",
  //       "$galleymode",
  //     ],
  //   });
  //   this.updateReportIndex(0);
  //   this.updateThemeIndex(0);
  // },
  // methods: {
  //   applyTheme(themeId) {
  //     const designerCss = require(`!!raw-loader!@grapecity/activereports/styles/${themeId}-designer.css`)
  //       .default;

  //     const viewerCss = require(`!!raw-loader!@grapecity/activereports/styles/${themeId}-viewer.css`)
  //       .default;

  //     const commonCss = require(`!!raw-loader!@grapecity/activereports/styles/${themeId}-ui.css`)
  //       .default;
  //     this.styles = `<style>${designerCss}</style><style>${viewerCss}</style><style>${commonCss}</style>`;
  //   },
  //   getReportDesign() {
  //     const report = this.reportsMap[this.currentReportIndex];
  //     return report.definition
  //       ? { reportDefinition: report.definition, displayName: report.label }
  //       : { id: report.url, displayName: report.label };
  //   },
  //   getReportPreview() {
  //     const report = this.reportsMap[this.currentReportIndex];
  //     return report.definition || report.url;
  //   },
  //   onRender(data) {
  //     this.reportsMap[this.currentReportIndex].definition = data.definition;
  //     this.$refs.reportViewer.Viewer().open(this.getReportPreview());
  //     this.previewMode = true;
  //     return Promise.resolve();
  //   },
  //   updateReportIndex(index) {
  //     this.currentReportIndex = index;
  //     this.$refs.reportViewer.open(this.getReportPreview());
  //     this.$refs.reportDesigner.setReport(this.getReportDesign());
  //   },
  //   currentThemeId() {
  //     return themes[this.currentThemeIndex || 0].id;
  //   },
  //   updateThemeIndex(index) {
  //     this.currentThemeIndex = index;
  //     this.applyTheme(this.currentThemeId());
  //   },
  // },
};
</script>

<style>
@import "https://cdn.materialdesignicons.com/2.8.94/css/materialdesignicons.min.css";
</style>

<style>


#viewer-host {
  width: 100%;
  height: 600px;
}
</style>
