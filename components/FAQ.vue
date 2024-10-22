<template>
    <div class="bg-gray-950 min-h-screen flex items-center justify-center" id="faq">
        <div class="md:p-8 mx-auto max-w-7xl flex flex-col md:flex-row">
            <div class="md:w-1/2 flex items-center justify-center w-full mt-6 md:mt-0 px-6 md:px-0">
                <img
                src="https://img.odcdn.com.br/cdn-cgi/image/width=1200,height=1200,fit=cover/wp-content/uploads/2024/08/desktop-apple.png"
                alt="Computador"
                    class="w-full h-auto rounded-lg shadow-md"
                />
            </div>
            <div class="md:w-1/2 p-4 flex flex-col items-center justify-center w-full">
                <h2 class="text-4xl font-bold text-white mb-6 text-center">Dúvidas Frequentes</h2>
                <Accordion type="single" class="w-full" collapsible :default-value="defaultValue">
                    <div class="space-y-4 w-full">
                        <AccordionItem v-for="item in accordionItems" :key="item.value" :value="item.value">
                            <AccordionTrigger
                                class="flex justify-between items-center p-4 bg-gray-700 rounded-lg border border-gray-600 hover:bg-gray-600 transition duration-200 ease-in-out">
                                <span class="text-lg font-semibold text-white text-left">{{ item.title }}</span>
                            </AccordionTrigger>
                            <AccordionContent
                                class="text-base p-4 text-gray-300 bg-gray-800 border-b border-l border-gray-600 rounded-b-lg transition duration-200 ease-in-out">
                                <p>{{ item.content }}</p>
                            </AccordionContent>
                        </AccordionItem>
                    </div>
                </Accordion>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from '@/components/ui/accordion';

const defaultValue = 'item-1';

const accordionItems = [
    { value: 'item-1', title: 'QUEM PODE PARTICIPAR?', content: 'Qualquer pessoa que realizar compras no valor total de R$ 500,00 em produtos eletrônicos.' },
    { value: 'item-2', title: 'COMO GANHAR NÚMEROS DE SORTE?', content: 'Para cada R$ 500,00 em compras, você receberá um número da sorte ao se cadastrar no site da promoção.' },
    { value: 'item-3', title: 'QUAL A DATA DO SORTEIO?', content: 'O sorteio será realizado no dia 05/01/2024, durante o evento ao vivo.' },
    { value: 'item-4', title: 'COMO FICAREI SABENDO SE GANHEI?', content: 'Os resultados serão divulgados no site da promoção e notificados por e-mail.' },
    { value: 'item-5', title: 'POSSO TROCAR O PRÊMIO POR DINHEIRO?', content: 'Não, os prêmios não podem ser trocados por dinheiro ou outro produto.' },
    { value: 'item-6', title: 'QUANTOS NÚMEROS DE SORTE POSSO TER?', content: 'Você pode acumular números da sorte para cada R$ 500,00 em compras realizadas.' },
    { value: 'item-7', title: 'COMO RECEBO MEU PRÊMIO?', content: 'Os prêmios serão enviados ao endereço cadastrado após a confirmação do sorteio.' },
    { value: 'item-8', title: 'O QUE FAÇO SE NÃO RECEBER O MEU PRÊMIO?', content: 'Caso não receba seu prêmio dentro do prazo informado, entre em contato com o suporte ao cliente através do nosso site.' },
];

</script>

<style scoped>
</style>