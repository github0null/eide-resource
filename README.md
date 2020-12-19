## index.json 接口

index.json 类型为 TemplateIndexDef 的 json 对象

```typescript

export type Category =
    '8051' | 'STM8' | 'PIC' | 'STM32' | 'MM32' | 'GD32' | 'NXP' | // vendor type
    'FreeRTOS' | 'uCOS-II' | 'RT-Thread-Nano' | // OS type

export interface CategoryInfo {
    display_name: string;
    description: string;
}

export interface TemplateInfo {

    file_name: string;

    display_name: string;

    category: string[];

    version: string;

    author: string | undefined;

    download_url: string | undefined;

    size: number | undefined;

    disabled: boolean | undefined;

    upload_time: string | undefined;

    update_time: string | undefined;
}

export interface TemplateIndexDef {
    category_map: { [name: string]: CategoryInfo };
    template_list: TemplateInfo[];
}

```
