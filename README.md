## index.json 接口

index.json 类型为 TemplateIndexDef 的 json 对象

```typescript

// 模板分类
export interface CategoryInfo {
    display_name: string;   // 用于显示的名称
    description: string;    // 简短的描述
}

export interface TemplateInfo {

    file_name: string; // 模板文件名

    display_name: string; // 用于显示的名称

    category: string[]; // 模板所属的分类

    version: string; // 版本

    author: string | undefined; // 作者名称
    
    upload_time: string | undefined; // 上传时间

    update_time: string | undefined; // 上次更新时间

    // ----- 忽略以下字段 -----------

    download_url: string | undefined;

    size: number | undefined;

    disabled: boolean | undefined;
}

export interface TemplateIndexDef {
    category_map: { [name: string]: CategoryInfo };
    template_list: TemplateInfo[];
}

```
