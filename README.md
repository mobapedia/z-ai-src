***files as of 6/24/26***  

index-zCAkFsQu.js is a base file  
jquery.min.js is a base file  

**index-zCAkFsQu.js loads:**  
DocxViewer-Db1C24Wi.js  
LoginLogo-D7FiGWqv.js  
PdfViewer-BEk7-Ig7.js  
PptxViewer-BpBxh4Gp.js  
XlsxUniverViewer-CNFhUAxc.js  
_page-B8UWV6qc.js  
_page-BKeZ528W.js  
_page-BR9pB3um.js  
_page-DRwlXLeC.js  
_page-Do2GpPDH.js  
chunk-FUIDI54P-BHKm7NI-.js  
diff-BrMgYGFR.js  
index-zCAkFsQu.js  
tippy.esm-CtJ-T4yr.js  

**then those load:**  
_getTag-TVuNWAcq.js  
pdf-BrxDJxgu.js  
jszip.min-DPBWOs5r.js  
_baseUniq-BMnx9epg.js  
tslib.es6-DE_iy5AC.js  
xlsx-DG2X6oDA.js  
index-C-J3cjKq.js  

**which in turn load:**  (CHECK THIS)  
index-B0qYmf3q.js  

**to load with these files, run this tampermonkey script (instant inject, run-at document-start)**:  
//observer.disconnect somewhere IDK  
new MutationObserver((mutationsList, observer) => {  
    for (const mutation of mutationsList) {  
        if (mutation.type === "childList" && mutation.addedNodes.length > 0) {  
            mutation.addedNodes.forEach((node) => {  
                if (node.tagName === "SCRIPT") {  
                    switch (node.src) {  
                        case "https://z-cdn.chatglm.cn/z-ai/frontend/prod-fe-1.1.67/assets/index-zCAkFsQu.js":  
                            node.src = "https://raw.githack.com/mobapedia/z-ai-src/main/index-zCAkFsQu.js"  
                            break  
                        case "https://o.alicdn.com/frontend-lib/common-lib/jquery.min.js":  
                            node.src = "https://raw.githack.com/mobapedia/z-ai-src/main/jquery.min.js"  
                    }  
                }  
            })  
        }  
    }  
}).observe(document, {  
    childList: true,  
    subtree: true  
})
