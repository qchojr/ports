# Created by: Alexey Dokuchaev <danfe@FreeBSD.org>

PORTNAME=	lzbench
PORTVERSION=	1.8.1
DISTVERSIONPREFIX=	v
CATEGORIES=	benchmarks

MAINTAINER=	danfe@FreeBSD.org
COMMENT=	In-memory benchmark of open-source LZ77/LZSS/LZMA compressors

BROKEN_riscv64=		fails to compile: invalid arch name 'native', string must begin with rv32{i,e,g} or rv64{i,g}

USES=		compiler:c11 gmake
USE_GITHUB=	yes
GH_ACCOUNT=	inikep

USE_HARDENING=	pie:off

PLIST_FILES=	bin/lzbench
PORTDOCS=	NEWS README.md

OPTIONS_DEFINE=	DOCS

post-patch:
	@${REINPLACE_CMD} -e '/PROGOS/s,Linux,${OPSYS},' \
		${WRKSRC}/_lzbench/lzbench.h

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/lzbench ${STAGEDIR}${PREFIX}/bin

do-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S,^,${WRKSRC}/,} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
