# final-pro
import requests

def get_global_warming_news():
    url = "https://api.globalwarmingnews.com/"
    response = requests.get(url)
    
    if response.status_code == 200:
        news = response.json()
        return news
    else:
        return "Ошибка при получении новостей о потеплении"

latest_news = get_global_warming_news()
print(latest_news)
